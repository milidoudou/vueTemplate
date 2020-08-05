<template>
  <div id="app">
    <t-form-item>
      <t-input placeholder='请输入' v-model="value"></t-input>
      {{value}}
    </t-form-item>
  </div>
</template>

<script>
import TInput from './components/t-input.vue'
import TFormItem from './components/t-form-item.vue'

export default {
  name: 'App',
  data() {
    return {
      value: 'qwe'
    }
  },
  components: {
    TFormItem,
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
