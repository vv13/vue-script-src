# vue-script-src
## Install
```
$ npm i vue-script-src
```

## Usage
First, register it for component:
```
import VueScriptSrc from 'vue-script-src'

export default {
  //...
  components: {
    VueScriptSrc,
  },
}
```
Then, use it in template:
```
<template>
<!-- ... -->
  <vue-script-src src="https://cdn.bootcss.com/jquery/3.3.1/jquery.min.js"></vue-script-src>
<!-- ... -->
</template>
```

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
