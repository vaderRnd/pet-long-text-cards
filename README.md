# Карточки с длинным текстом

Пет-проект: карточки с раскрывающимся длинным текстом. Реализовано только на HTML и CSS, без JavaScript.

## Демо

Открыть `index.html` в браузере.

## Как это работает

Раскрытие текста реализовано через скрытый `<input type="checkbox">` и CSS-селектор `:checked`:

- по умолчанию `.card__content` имеет `max-height: 100px` — текст обрезан
- при клике на кнопку `<label>` переключает связанный чекбокс
- `card__toggle:checked ~ .card__content` снимает ограничение высоты
- текст кнопки меняется между «Expand» и «Collapse» через `display: none` на соответствующих `<span>`

## Структура проекта

```
├── index.html       # разметка карточек
├── css/
│   └── styles.css   # все стили
└── img/             # изображения для карточек
```

## Структура карточки

```html
<article class="card">
  <input type="checkbox" class="card__toggle" id="ct-1" />
  <img src="..." alt="..." />
  <h2>Заголовок</h2>
  <p class="card__content">Длинный текст...</p>
  <label for="ct-1" class="card__button">
    <span class="card__button-text-expand">Expand</span>
    <span class="card__button-text-collapse">Collapse</span>
  </label>
</article>
```

Для добавления новой карточки нужно скопировать блок выше и задать уникальный `id` чекбоксу и соответствующий `for` у `<label>`.

## Технологии

- HTML5
- CSS3 (Flexbox, псевдокласс `:checked`)
