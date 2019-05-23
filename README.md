# vue-decorate-html-without-v-html

Demo: Avoid to XSS on decorating for user input.

Visit: <https://vue-decorate-html-without-v-html.netlify.com/>

- [src/components/UnSafeBold.vue](src/components/UnSafeBold.vue) has a vulnerability.
- [src/components/SafeBold.vue](src/components/SafeBold.vue) is safe implementation, but a bit complex.

## XSS vector

Input: `<script>alert(1)</script>` 


## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn run serve
```

### Compiles and minifies for production
```
yarn run build
```

### Run your tests
```
yarn run test
```

### Lints and fixes files
```
yarn run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
