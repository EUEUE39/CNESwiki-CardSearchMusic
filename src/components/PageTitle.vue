<template>
  <div class="background">
    <div class="title" ref="ipt">
      CardSearch!!
      <!--  A.SUBARU-->
    </div>
    <div class="subscript">
    </div>
  </div>
</template>

<script>
export default {
  name: "PageTitle",
}
</script>

<style scoped>
/*.background{*/
/*  display: flex;*/
/*}*/

.title {
  color: white;
  font-weight: bolder;
  font-size: 100px;
  writing-mode: tb-rl;
  position: absolute;
  z-index: 1;
  margin: 20px 0;
  left: 0;
  bottom: 0;
}

.subscript{
  position: absolute;
  right: 30px;
  bottom: 30px;
  height: 0;
  width: 0;
  /*border:  solid 30px;*/
  border-bottom: 20vh solid rgb(253,239,11);
  border-left: 20vh solid transparent;
}
</style>