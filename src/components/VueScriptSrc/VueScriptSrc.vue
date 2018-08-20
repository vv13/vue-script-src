<script>
export default {
  name: "vue-script-src",

  render(createElement) {
    return createElement("div", {
      class: "vue_script_src",
      ref: "wrap",
      style: { display: "none" }
    });
  },

  props: {
    sources: {
      type: Array,
      default: () => []
    },

    source: {
      type: String
    }
  },

  data() {
    return {
      cursor: 0
    };
  },

  methods: {
    loadScriptSimple() {
      const dom = document.createElement("script");
      dom.type = "text/javascript";
      dom.src = src;
      dom.onload = () => {
        this.$emit("completed");
      };
      this.$refs.wrap.appendChild(dom);
    },

    loadScript(src) {
      const dom = document.createElement("script");
      dom.type = "text/javascript";
      dom.src = this.sources[this.cursor];
      dom.onload = () => {
        this.loadNext();
      };
      dom.onerror = e => {
        console.error(e);
      };
      this.$refs.wrap.appendChild(dom);
    },

    loadNext() {
      this.cursor += 1;
      if (this.cursor < this.sources.length) this.loadScript();
      if (this.cursor === this.sources.length) this.$emit("completed");
    }
  },

  created() {
    if (
      (!this.source && !this.sources.length) ||
      (this.source && this.sources.length)
    ) {
      throw new Error("Pass source or sources only one");
    }
  },

  mounted() {
    if (this.source) this.loadScriptSimple(this.source);
    this.sources.forEach(source => this.loadScript(source));
  }
};
</script>

