<template>
  <div ref="wrap" class="vue_script_src" style="display: none"></div>
</template>
<script>
export default {
  name: 'vue-script-src',
  props: {
    src: {
      type: String
    }
  },
  mounted() {
    const dom = document.createElement("script");
    dom.type = "text/javascript";
    dom.src = this.src;
    this.$refs.wrap.appendChild(dom);
  }
};
</script>

