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


      <div type="button" class="btn btn-primary" data-toggle="modal" data-target="#centralModalDanger" v-b-modal.centralModalDanger>Launch
        modalabc
      </div>
      <search-query-window></search-query-window>

      <button type="button" class="btn btn-primary" data-toggle="modal" data-target=".bd-example-modal-xl" v-b-modal.bd-example-modal-xl>Extra large modal</button>

      <div class="modal fade bd-example-modal-xl" tabindex="-1" role="dialog" aria-labelledby="myExtraLargeModalLabel" id="bd-example-modal-xl" aria-hidden="true">
        <div class="modal-dialog modal-xl">
          <div class="modal-content">
            ...
          </div>
        </div>
      </div>

    </div>

  </div>
</div>
</template>

<script>
import SearchButton from "@/components/SearchButton";
import SearchQueryWindow from "@/components/SearchQueryWindow";

export default {
  name: "MainPage",
  components: {
    SearchButton,
    SearchQueryWindow,
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

.panel-heading {
  border-top-left-radius: inherit;
  border-top-right-radius: inherit;
}
</style>