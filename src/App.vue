<template>
  <div id="app">
    <form-component>
      
    </form-component>
  </div>
</template>

<script>
import FormComponent from "./components/FormComponent"
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
    FormComponent
  }
}
</script>

<style lang="scss">

</style>
