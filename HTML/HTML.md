## HTML
**1. Что такое HTML и для чего он используется?**
> Hyper text markup language/язык гипертекстовой разметки. Стандартизированный язык, позволяющий составлять форматированный текст. Данный текст интерпретируется браузером. После браузер отображает его на экране в виде элементов web-страницы. Скелет или каркас, содержащий разметку.

**2. Что такое doctype и для чего он используется?**
> Указание типа документа. Добавляется первой строкой любого html документа. Служит для того, чтобы браузер мог понять, как ему интерпретировать страницу и в соответствии с каким стандартом осуществлять парсинг документа.

**3. Что такое семантика? Какие семантичные тэги знаете?**
> Использование правильных тегов, описывающих содержимое контента внутри себя. Семантичный тег - носит смысловое объяснение. Если блок текста, то он должен быть обернут в тег `<p></p>`.

**4. Какая разница между тэгами `<strong><em>` и `<b><i>`?**
> `<strong>` и `<b>` делают текст жирным, `<em>` и `<i>` курсивным. Однако `<strong><em>` используют для добавления элементу логического выделения (роботы и скринридеры сделают акцент), в то время как `<b><i>` просто визуальный вид без добавления семантики.

**5. Расскажите о meta-тэге с name=”viewport”?**
> Используется для построения отзывчивой версии сайта (оптимизация для mobile device). **Content** - как страница должна себя вести на устройствах с разным расширением. **Width** - определяет размер окна просмотра. **Device-width** - в масштабе 100%. **Inital-scale** - уровень масштабирования при первой загрузке. 

**6. Что описывается в тэге `<head>`**
> `<title>` основной заголовок html страницы. `<meta>` - указание кодировки, ключевых слов, указание вспомогательных механизмов для браузеров и устройств. Путь к таблице стилей `<link>` и шрифтов. Скрипты. 

**7. Основные этапы проверок валидности HTML документа**
> 1. Document type definition (dtd)
> 2. Валидация синтаксиса
> 3. Проверка вложенности 
> 4. Проверка на посторонние элементы

**8. Что такое ApplicationCache в HTML**
> 1. Автономный просмотр
> 2. Ресурсы кэшируются локально, загрузка быстрее
> 3. Снижение нагрузки на сервер. Браузер загружает с сервера только измененные ресурсы.

**9. Базовая структура HTML-страницы**
```html
<!Doctype html>
<html language="en">
<head>
  <meta charset="UTF-8">
  <title></title>
</head>
<body>
  //content
</body>
</html>
```

**10. Что такое инлайновый стиль? Можно ли его переопределить? Есть ли у HTML элементов свои дефолтные стили?**
> Стиль, примененный к определенному элементу указывается в html с помощью атрибута `<style>`. Переопределить можно с помощью директивы `!important`. Дефолтные стили отличаются в браузерах, для этого используют **normalize.css**.

**11. Как семантически правильно сверстать картинку с подписью? Для какого тэга используется атрибут alt и зачем он нужен?**
> Атрибут alt используется если не отображается изображение. В таком случае отобразится текст, описывающий содержимое картинки. Улучшает доступность страницы.
```html
<figure>
	<img src=”” alt=”image description”>
	<figcaption>Description</figcaption>
</figure>
```

**12. Что такое валидация? Типы проверок HTML документа?**
> Валидация – проверка прогой на соответствие установленным web стандартам и обнаружение ошибок. Эта спецификация разработана консорциумом www. 
> Этапы проверки:
> 1. Тип документа (dtd – document type definition)
> 2. HTML код на ошибки и правильность (проверка синтаксиса)
> 3. Вложенность и имена тегов
> 4. Посторонние элементы 

**13. Какой тег использовать для того, чтоб сверстать кнопку?**
> 1. Default button
```html
<button type=”button”>btn</button>
```
> 2. Submit button
```html
<button type=”submit”>btn</button>
```
> 3.Input type button
```html
<input type=”button” /> 
```
> 4.Input type submit
```html
<input type=”submit” value=”button” /> 
```
> 5. Link button 
```html
<a href=”#”>button</a>
```

**14. Типы `input` элементов в HTML?**
> Для получения вводимых данных используется атрибут type=” ” в input
> 1. Text
> 2. Password
> 3. Email
> 4. Number
> 5. Submit
> 6. Checkbox
> 7. Radio
> 8. Date
> 9. Month
> 10. Local
> 11. Daytime
> 12. Reset
> 13. Submit
> 14. Button
> 15. Search
> 16. Tel и т.д

**15. Разница между `<script>`, `<script async>` и `<script defer>`?**
> `<script async>` - для скриптов, независимых от других скриптов. Например аналитика. `<script defer>` - будет исполнен при чтении HTML страницы. Однако выполнение произойдет после парсинга. Почти идентичен обычному `<script>`. Используется со скриптами, где интегрирована логика взаимодействия с DOM элементами.

**16. Для чего используется тег `<picture>`?**
> Когда для разных устройств нужны разные картинки. Он служит контейнером для одного и более элементов source и одного элемента img
```html
<picture>
	<source>
  <source>
  <img>
</picture>
```

**17. Типы списков в HTML?**
> 1. Маркированный список:
```html
<ul>
  <li>text</li> //● text
  <li>text</li>
  <li>text</li>
</ul>
```
> 2. Нумерованный список:
```html
<ol>
  <li>text</li> //1. text
  <li>text</li>
  <li>text</li>
</ol>
```
> 3. Список определений:
```html
<dl>
  <dt>text</dt>
  <dd>the written words</dd>
</dl>
```
**18. Для чего используется тег `<datalist>`?**
> Тег для создания выпадающего списка
```html
<datalist>
	<option value=””>
  <option value=””>
</datalist>
```

**19. Что такое элемент output в HTML?**
> Отображение суммы чисел

**20. Что такое элемент `<canvas>`?**
> Холст. HTML элемент для вставки изображений, градиентов и сложной анимации. Область, где с помощью JavaScript можно рисовать объекты, преобразовывать их. Низкоуровневый API для отрисовки графики.

**21. Что такое svg и canvas? Разница между и в каких случаях лучше использовать?**
> 1. SVG – язык разметки масштабируемой графики. Набор элементов. Векторная графика. Плох для игры. Низкая скорость рендеринга. 
> 2. CANVAS – html элемент, используется для рисования графики, чаще всего в играх. Одиночный DOM элемент. Нет API для анимации. 

**22. Для чего используются теги `<tr>`, `<th>` и `<td>`?**
> Несамостоятельный теги. Используются в связке с `<table>`. 
> 1. `<tr>` -  строка таблицы (table row)
> 2. `<th>` - заголовок (table head)
> 3. `<td>` - ячейка таблицы (table data)

**23. Что такое мета теги?**
> Внутри тега `<head>` описывают содержимое страницы. Не отображается в браузере. Нужны для поисковых систем. 
> 1. Кодировка `charset=”UTF-8”`
> 2. SEO информация
> 3. Вспомогательные механизмы для браузеров и устройств

**24. Почему хорошей практикой считается располагать `<link>` для подключения CSS стилей внутри тега `<head>`, а `<script>` для подключения JavaScript ставить перед закрывающимся тегом `</body>`?**
> Описано спецификацией. Чтение страницы слева –> направо, сверху | вниз. Когда браузер встречает тег `<script>`, все процессы построения DOM и стилизация элементов откладывается до тех пор, пока найденный скрипт не будет исполнен. Чтоб пользователь при загрузке страницы не видел контент без стилей, их указывают в `<link>`.

**25. Для чего нужен атрибут autocomplete?**
> Нативная поддержка автозаполнения. Может отключаться в настройках браузера. Атрибут с параметром on/off. 

**26. Для чего используются теги `<sub>`, `<sup>`?**
> 1. `<sub>` - степень
> 2. `<sup>` - индекс

**27. Как семантически правильно сверстать меню?**
```html
<nav>
	<ul>
		<li><a href=”#”>text</a></li>
		<li><a href=”#”>text</a></li>
	</ul>
</nav>
```