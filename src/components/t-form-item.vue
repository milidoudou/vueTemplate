<template>
  <div>
    <slot></slot>
  </div>
</template>

<script>
import Schema from 'async-validate'

export default {
  props: {
    label: {
      type: String,
      default: ''
    },
    prop: {
      type: String,
      default: ''
    }
  },
  data() {
    return {}
  },
  methods: {
    validate() {
      const 
    }
  }
}
</script>

<style>

</style>