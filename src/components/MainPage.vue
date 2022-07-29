<template>
<div class="mainPage">
  <div class="header">
    <SearchButton></SearchButton>
  </div>
  <div class="card">
    <div>
      <b-button v-b-modal.modal-1>Launch demo modal</b-button>

      <b-modal id="modal-1" title="BootstrapVue">
        <p class="my-4">Hello from modal!</p>
      </b-modal>
    </div>

  </div>
</div>
</template>

<script>
import SearchButton from "@/components/SearchButton";


export default {
  name: "MainPage",
  components: {
    SearchButton
  }
}
</script>

<style scoped>
/*.header{*/
/*  !*float:left;*!*/
/*  display: flex;*/
/*  justify-content: flex-end ;*/
/*}*/



.mainPage{
  /*border:10px solid white;*/
  /*background:rgb(124,127,132);*/
  /*height: 100%;*/
  /*width:100%;*/
}
</style>