<template>
<div class="mainPage">
  <div class="header">
    <SearchButton></SearchButton>
  </div>
  <div class="card">
    <div>


    </div>

  </div>
</div>
</template>

<script>
import SearchButton from "@/components/SearchButton";

export default {
  name: "MainPage",
  components: {
    SearchButton,
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