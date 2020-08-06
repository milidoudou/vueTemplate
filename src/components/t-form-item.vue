<template>
  <div>
    {{label}} <slot></slot>
  </div>
</template>

<script>
import Schema from 'async-validator'

export default {
  name: 't-form-item',
  inject: ['form'],
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
  mounted() {
    this.$on('input', (e) => {
      this.validate(e)
    })
  }, 
  methods: {
    async validate(e) {
      
      const descriptor  = {
        [this.prop]: this.form.rules[this.prop]
      }
      const validator = new Schema(descriptor)
      try {
        await  validator.validate({
          [this.prop]: e
        })
      } catch ({errors, fileds}) {
        // console.log('error', error)
        console.log('errors', errors, fileds)
      }
      

      validator.validate({
        [this.prop]: e
      }).then((success) => {
        console.log('success', success)
      }).catch(({errors, fileds}) => {
        console.log('errors', errors, fileds)
      })

    }
  }
}
</script>

<style>

</style>