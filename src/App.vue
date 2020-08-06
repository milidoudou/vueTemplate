<template>
  <div id="app">
    <t-form v-model="form" :rules='rules'>
      <t-form-item prop='value' label='value值:'>
        <t-input placeholder='请输入' v-model="form.value"></t-input>
      </t-form-item>
    </t-form>
  </div>
</template>

<script>
import TForm from './components/t-form'
import TInput from './components/t-input.vue'
import TFormItem from './components/t-form-item.vue'

export default {
  name: 'App',
  data() {
    return {
      rules: {
        value: [
          {required: true, message: 'value必填'}
        ]
      },
      form: {
        value: 'qwe'
      }
     
    }
  },
  components: {
    TFormItem,
    TForm,
    TInput
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
