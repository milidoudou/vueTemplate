<template>
  <div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    model: {
      type: Object,
      default: () => {}
    },
    rules: {
      type: Object,
      default: () => {}
    }
  },
  provide() {
    return {
      form: this
    }
  },
  data() {
    return {}
  },
  methods: {}
}
</script>

<style>

</style>