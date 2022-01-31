<template>
  <div id="app">
      <header-box />
      <main-container :discList = "discList"/>
      <loader-box v-if="loader()"/>
  </div>
</template>

<script>
import headerBox from './components/headerBox.vue'
import mainContainer from './components/mainContainer.vue'
import axios from 'axios'
import loaderBox from './components/loaderBox.vue'


export default {
  name: 'App',
  components: {
      headerBox,
      mainContainer,
      loaderBox,
  },
  data(){
    return{
      discList: [],
    }
  },
  methods: {
    loader: function(){
      if(this.discList.length != 10){
        return true;
      }else{
        return false;
      }
    },
    testLoader: function(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response)=>{
        this.discList = response.data.response;
    })
    }
  },
  mounted(){
      setTimeout(this.testLoader,5000);
  }
}
</script>

<style lang="scss">
  @import './style/main.scss'
</style>
