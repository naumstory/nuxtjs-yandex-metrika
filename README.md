# Yandex Metrika

[![npm](https://img.shields.io/npm/dt/@naumstory/nuxtjs-yandex-metrika.svg?style=flat-square)](https://www.npmjs.com/package/@naumstory/nuxtjs-yandex-metrika)
[![npm (scoped with tag)](https://img.shields.io/npm/v/@naumstory/nuxtjs-yandex-metrika/latest.svg?style=flat-square)](https://www.npmjs.com/package/@naumstory/nuxtjs-yandex-metrika)

## Апгрейд

В оригинальной версии плагин по каким-то причинам не добавлял атрибуты к подключаемому скрипту метрики. Я говорю об async и rel="preload".

Async был прописан, но без указания значения, а таким образом, при генерации проекта, скрипт не подхватывал атрибут async, считая его пустым. Я поправил этот момент тем, что добавил значение true.

Так же был добавлен важный атрибут rel со значением preload.

> Добавьте Яндекс Метрику в ваше приложение nuxt.js

Этот плагин автоматически отправляет события первой страницы и изменения маршрута в Яндекс Метрику.

**Примечание:** яндекс метрика не включена в режиме dev.
Вы можете установить переменную окружения `NODE_ENV` на `production` для тестирования в режиме dev.

## Установка и настройка

- Добавьте модуль `@naumstory/nuxtjs-yandex-metrika` в свой проект

```js
npm i @naumstory/nuxtjs-yandex-metrika

// or

yarn add @naumstory/nuxtjs-yandex-metrika
```

- Добавьте `@naumstory/nuxtjs-yandex-metrika` в массив `modules` в конфиге nuxt.js `nuxt.config.js`

```js
{
  modules: [
    [
      '@naumstory/nuxtjs-yandex-metrika',
      {
        id: 'XXXXXX',
        webvisor: true
        // clickmap:true,
        // useCDN:false,
        // trackLinks:true,
        // accurateTrackBounce:true,
      }
    ]
  ];
}
```

## Опции

Дополнительная информация:

- [Документация Яндекс.Метрика](https://yandex.com/support/metrica/code/counter-initialize.xml)
- [hit метод](https://yandex.com/support/metrica/objects/hit.xml)

### `id`

- Обязательный

### `webvisor`

### `clickmap`

### `trackLinks`

### `accurateTrackBounce`
