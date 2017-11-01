# vue-datetime
> Mobile friendly datetime picker for Vue. Supports date, datetime and time modes, i18n and disabling dates.

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Latest Version on NPM](https://img.shields.io/npm/v/vue-datetime.svg?style=flat-square)](https://npmjs.com/package/vue-datetime)
[![npm](https://img.shields.io/npm/dt/vue-datetime.svg?style=flat-square)](https://www.npmjs.com/package/vue-datetime)

## Demo

[![demo](https://raw.githubusercontent.com/mariomka/vue-datetime/master/docs/demo.gif)](http://mariomka.github.io/vue-datetime)

**[Go to demo](http://mariomka.github.io/vue-datetime)**.

# Install

yarn

```bash
yarn add vue-datetime
```

npm

```bash
npm install vue-datetime --save
```

## Register the component

```js
import Datetime from 'vue-datetime';

Vue.use(Datetime);
```

### Register manually

#### Global

```js
import { Datetime } from 'vue-datetime';

Vue.component('datetime', Datetime);
```

#### Local

```js
import { Datetime } from 'vue-datetime';

Vue.extend({
  template: '...',
  components: {
    datetime: Datetime
  }
});
```

## Usage

### Minimal

```html
<datetime v-model="date"></datetime>
```

### Full

```html
<datetime v-model="date"
          type="datetime"
          input-format="DD-MM-YYYY HH:mm"
          wrapper-class="my-wrapper-class"
          input-class="my-input-class"
          placeholder="Select date"
          locale="es"
          :disabled-dates="['2017-09-07', ['2017-09-25', '2017-10-05']]"
          monday-first
          auto-continue
          auto-close
          required></datetime>
```

## Params

Parameter | Type | Default
--------- | ---- | ------
v-model (*required*) | `String` | -
type | `String`: *date*, *datetime* or *time* | `date`
input-format | `String` | `YYYY-MM-DD`, `YYYY-MM-DD HH:mm` or `HH:mm`
wrapper-class | `String` | `null`
input-class | `String` | `null`
placeholder | `String` | `null`
locale | `String` | `null`
disabled-dates | `Array` | `[]`
monday-first | `Boolean` | `false`
auto-continue | `Boolean` | `false`
auto-close | `Boolean` | `false`
required | `Boolean` | `false`

The component is based on [Moment.js](https://momentjs.com), check out documentation to set `input-format` and `locale`.

## Events

Components emit the `input` event.

# License

[The MIT License](http://opensource.org/licenses/MIT)
