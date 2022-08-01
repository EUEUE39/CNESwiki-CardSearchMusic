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
#app {
  border:30px solid white;
  background:rgb(228,232,233);
  height: calc(100vh - 60px );
  width: auto;
  /*padding: 0 20vh;*/
  margin:0;
  box-sizing: unset;
}
</style>
