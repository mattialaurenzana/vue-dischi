<template>
  <div id="app">
      <header-box />
      <main-container :discList = "discList"/>
  </div>
</template>

<script>
import headerBox from './components/headerBox.vue'
import mainContainer from './components/mainContainer.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
      headerBox,
      mainContainer
  },
  data(){
    return{
      discList: [],
    }
  },
  mounted(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response)=>{
      this.discList = response.data.response;
    })
  }
}
</script>

<style lang="scss">
  @import './style/main.scss'
</style>
