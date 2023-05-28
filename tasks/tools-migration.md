### Какого рода задача?
Мигрировать авторизацию на tools

###  Что и где будем менять?
Для сборки приложения необходимо использовать `yarn service build`, для запуска в дев режиме - `yarn service dev`

Необходимо оформить файл auth как пакет (воркспейс) с определенной структурой: директория `src` и `index.ts` внутри - [пример](https://github.com/atls/hyperion/blob/master/ui-parts/button/package.json)

Внутри package.json должны находится скрипты для запуска проекта - `build`, `dev` и `start`

- `build` билдит проект через `yarn service build` и кладет js в папку `dist`
- `dev` запускает проект в dev режиме
- `start` запускает уже сбилженный проект (`node dist/index.js`)

[Краткий обзор tools](https://github.com/atls/tools/wiki)

### Укажите референс
Приведение проекта к общему стеку

Пример приложения, собирающегося с помощью `yarn service` - https://github.com/atls/project-starter/blob/master/gateway/entrypoints/public/package.json

Пример библиотеки, которая будет публиковаться в npm регистр - https://github.com/atls/nextjs/blob/master/packages/next-sitemap-generator/package.json
