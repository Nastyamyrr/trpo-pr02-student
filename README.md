# Практическая работа №2 — CSS, адаптивная верстка и SCSS

Адаптивный каталог учебных товаров на HTML, SCSS и JavaScript. Используются все 18 записей из `data/catalog.csv` и параметры из `data/theme.json`.

## Структура
`index.html`, `scss/` (variables, mixins, base, layout, components, styles.scss), `css/styles.css`, `js/app.js`, `images/`, `data/`, `package.json`.

## Реализовано
- 18 карточек из dataset; поиск, категория, максимальная цена и сортировка;
- состояние «Ничего не найдено» и состояние ошибки загрузки;
- CSS Grid и Flexbox; два breakpoint: 900px и 600px;
- SCSS-переменные для цветов, отступов, радиуса и контейнера; вложенность; mixins; функция `rem()`;
- исходные SCSS и скомпилированный CSS; относительные пути к изображениям.

## Как данные попадают в интерфейс
`js/app.js` загружает `data/catalog.csv` и `data/theme.json`, разбирает CSV в `parseCsv()`, создаёт категории, затем `apply()` фильтрует данные, а `render()` создаёт карточки. При ошибке загрузки показывается отдельный блок.

## Запуск
Из корня проекта: `python3 -m http.server 8000`, затем открыть `http://localhost:8000`. Для SCSS: `npm install`, затем `npm run build`; для наблюдения: `npm run watch`. Готовый `css/styles.css` уже включён, поэтому GitHub Pages работает без сборки.

## Адаптивность
Проверить 375, 768 и 1440 px. На мобильном фильтры переходят над каталогом, карточки становятся одной колонкой, горизонтального скролла нет.

## Контроль
Проверить загрузку 18 товаров, фильтры, сортировку, пустой результат и ошибку dataset.

## SCSS и CSS custom properties
SCSS-переменные обрабатываются при компиляции, а CSS custom properties (`--name`) существуют в браузере и могут изменяться во время работы страницы.

## Git
Рекомендуется минимум четыре осмысленных коммита: `feat: add project structure and dataset`; `feat: add adaptive catalog layout`; `feat: add scss architecture and responsive styles`; `feat: add dataset filters and states`.
