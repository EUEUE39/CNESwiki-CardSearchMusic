<template>
<!--  <img alt="Vue logo" src="./assets/logo.png">-->
<!--  <HelloWorld msg="Welcome to Your Vue.js App"/>-->

  <page-title></page-title>
  <MainPage></MainPage>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import MainPage from './components/MainPage'
import PageTitle from "@/components/PageTitle";


export default {
  name: 'App',
  components: {
    // HelloWorld,
    MainPage,
    PageTitle,
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
  /*margin-top: 60px;*/

}
body {
  border:30px solid white!important;
  background:rgb(228,232,233)!important;
  height: calc(100vh - 60px )!important;
  width: auto!important;
  /*padding: 0 20vh;*/
  margin:0!important;
  box-sizing: unset!important;
}
</style>
