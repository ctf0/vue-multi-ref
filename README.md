<h1 align="center">
    Vue Multi Ref
    <br>
    <a href="https://www.npmjs.com/package/vue-multi-ref"><img src="https://img.shields.io/npm/v/vue-multi-ref.svg?style=for-the-badge" alt="npm" /></a> <a href="https://www.npmjs.com/package/vue-multi-ref"><img src="https://img.shields.io/npm/dt/vue-multi-ref.svg?style=for-the-badge" alt="npm" /></a>
</h1>

This is a directive to help use same `ref` on more than one element.

Big thanx to [@Herteby](https://github.com/herteby) & [@LinusBorg](https://github.com/LinusBorg). :fire::metal::clap:

[original post](https://forum.vuejs.org/t/how-to-use-the-same-ref-for-more-than-one-item/22481).

## Installation

```bash
npm install vue-multi-ref --save
```

## Usage

- register the directive

    ```js
    import Vue from 'vue'
    import VueMultiRef from 'vue-multi-ref'

    Vue.use(VueMultiRef)
    new Vue({ el: '#app' })
    ```

    or using Vue as global variable

    ```js
    window.Vue = require('vue')
    require('vue-multi-ref')

    new Vue({ el: '#app' })
    ```

- now add `v-multi-ref:refName` to any number of elements that you want to have the same ref, ex.
    + `refName` could be
        - camelCase = `refName`
        - kebab-case = `ref-name`
        - snake-case = `ref_name`

    ```html
    <div v-multi-ref:my-ref>a</div>
    <li v-multi-ref:my-ref>b</li>
    <a v-multi-ref:my-ref>c</a>
    ```

- result

    ```js
    // console.log(this.$refs['my-ref'])

    > my-ref: (3) [div, li, a]
    ```
    
### Security

If you discover any security-related issues, please email [ctf0-dev@protonmail.com](mailto:ctf0-dev@protonmail.com).
