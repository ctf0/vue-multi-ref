# Vue Multi Ref

[![npm](https://img.shields.io/npm/v/vue-multi-ref.svg?style=for-the-badge)](https://www.npmjs.com/package/vue-multi-ref) [![npm](https://img.shields.io/npm/dt/vue-multi-ref.svg?style=for-the-badge)](https://www.npmjs.com/package/vue-multi-ref)

This is a directive to help use same `ref` on more than one element.

Big thanx to [@Herteby](https://github.com/herteby) & [@LinusBorg](https://github.com/LinusBorg). :fire::metal::clap:

[original post](https://forum.vuejs.org/t/how-to-use-the-same-ref-for-more-than-one-item/22481).

## Installation

```bash
npm install vue-multi-ref --save
```

## Usage

**1-** register the directive

```js
window.Vue = require('vue')
require('vue-multi-ref')

new Vue({
    el: '#app',
})
```

**2-** now add `v-multi-ref="'refName'"` to any number of elements that you want to have the same ref, ex.

```html
<div v-multi-ref="'ref1'">a</div>
<li v-multi-ref="'ref1'">b</li>
<a v-multi-ref="'ref1'">c</a>
```

- result
```js
// console.log(this.$refs.ref1)

> ref1: (3) [div, li, a]
```
