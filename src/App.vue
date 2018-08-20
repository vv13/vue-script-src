<template>
  <div id="app">
    <vue-script-src
      @completed="handleCompleted"
      :sources="sources">
    </vue-script-src>
  </div>
</template>

<script>
import VueScriptSrc from "./components/VueScriptSrc";

export default {
  name: "app",

  data() {
    return {
      sources: [
        "https://cdn.bootcss.com/jquery/3.3.1/jquery.min.js",
        "/test1.js"
      ]
    };
  },
  components: {
    VueScriptSrc
  },
  methods: {
    handleCompleted() {
      console.log("completed!");
    }
  }
};
</script>
