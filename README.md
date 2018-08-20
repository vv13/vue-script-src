# vue-script-src
在Vue组件中加载异步脚本的正确姿势。

## 安装
### npm
```
$ npm i vue-script-src
```

## 使用
### 示例
```
<template>
  <div id="app">
    <vue-script-src
      :sources="['https://cdn.bootcss.com/jquery/3.3.1/jquery.min.js']"
      @completed="handleCompleted"
    ></vue-script-src>
  </div>
</template>

<script>
import VueScriptSrc from './components/VueScriptSrc'

export default {
  components: {
    VueScriptSrc,
  },
  methods: {
    handleCompleted() {
      console.log('completed')
    },
  },
}
</script>
```

### Props
#### sources
- 类型：Array
- 默认值：[]
- 说明: 异步脚本源地址数组，按照传入顺序进行加载

#### source
- 类型：String
- 说明: 异步脚本源地址

### Event
#### completed
- 类型：Function
- 说明：传入脚本加载成功后执行


