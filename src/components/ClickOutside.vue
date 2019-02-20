<script>
export default {

  props: {
    do: {
      type: Function,
      default () {
        return () => {};
      }
    }
  },
  methods: {
    handleClickOutside (e) {
      if (this.$el.contains(e.target)) {
        return;

      }
      this.do();
    }
  },
  mounted () {
    document.addEventListener('click', this.handleClickOutside);
    this.$once('hook:beforeDestroy', () => {
      document.removeEventListener('click', this.handleClickOutside);
    });
  },
  render (createElement) {
    return this.$slots.default[0];
  }
};
</script>
