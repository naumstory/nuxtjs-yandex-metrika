# Yandex Metrika

[![npm](https://img.shields.io/npm/dt/@naumstory/nuxtjs-yandex-metrika.svg?style=flat-square)](https://www.npmjs.com/package/@naumstory/nuxtjs-yandex-metrika)
[![npm (scoped with tag)](https://img.shields.io/npm/v/@naumstory/nuxtjs-yandex-metrika/latest.svg?style=flat-square)](https://www.npmjs.com/package/@naumstory/nuxtjs-yandex-metrika)

## Апгрейд

В оригинальной версии плагин по каким-то причинам не добавлял атрибуты к подключаемому скрипту метрики. Я говорю об async и rel="preload".

Async был прописан, но без указания значения, а таким образом, при генерации проекта, скрипт не подхватывал атрибут async, считая его пустым. Я поправил этот момент тем, что добавил значение true.

Так же я добавил важный атрибут rel со значением preload.

> Add Yandex Metrika to your nuxt.js application.

This plugins automatically sends first page and route change events to yandex metrika.

**Note:** yandex metrika is not enabled in dev mode.
You can set environment variable `NODE_ENV` to `production` for testing in dev mode.

## Setup

- Add `@naumstory/nuxtjs-yandex-metrika` dependency using yarn or npm to your project
- Add `@naumstory/nuxtjs-yandex-metrika` to `modules` section of `nuxt.config.js`

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

## Options

For more information:

- [Documetation for Ya.Metrika](https://yandex.com/support/metrica/code/counter-initialize.xml)
- [hit method](https://yandex.com/support/metrica/objects/hit.xml)

### `id`

- Required

### `webvisor`

### `clickmap`

### `trackLinks`

### `accurateTrackBounce`
