<template>
  <div class="search-query-box">
    <div class="SearchButton">
      <div>
        搜索
      </div>
    </div>
    <div class="SearchButton" v-on:click="rarityOAdd=!rarityOAdd">
      <div v-if=rarityOAdd>稀有度</div>
      <div v-else>追加顺</div>
    </div>
    <div class="SearchButton" v-on:click="desc=!desc">
      <div v-if=rarityOAdd>
        <div v-if=desc>从高到低</div>
        <div v-else>从低到高</div>
      </div>
      <div v-else>
        <div v-if=desc>从新到旧</div>
        <div v-else>从旧到新</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SearchButton",
  data() {
    return {
      rarityOAdd: false,
      desc: true,
    }
  }
}
</script>

<style scoped>
.search-query-box {
  display: flex;
  justify-content: flex-end;
}

.SearchButton {
  border-radius: 15px 2px 2px 2px;
  border: 3px solid;
  border-color: rgb(45, 60, 168) rgb(23, 34, 95) rgb(23, 34, 95) rgb(45, 60, 168);

  font-size: larger;
  font-weight: bolder;

  padding: 7px 0;

  width: 120px;

  background: rgb(254, 254, 254);
  color: rgb(13, 28, 92);

  box-shadow: 3px 5px 6px rgba(0, 0, 0, 0.2);
  margin: 0 10px;

  transition: 0.1s;   /* 缩放动画特效时间*/
}
.SearchButton:active{
  transform: scale(0.95);
}

.SearchButton div {
  -moz-user-select: none; /*火狐*/
  -webkit-user-select: none; /*webkit浏览器*/
  -ms-user-select: none; /*IE10*/
  -khtml-user-select: none; /*早期浏览器*/
  user-select: none;

}
</style>