<template>
  <div>
    <!-- Central Modal Medium Danger -->
    <div class="modal fade" id="centralModalDanger" tabindex="-1" role="dialog" aria-labelledby="myModalLabel"
         aria-hidden="true">
      <div class="modal-dialog modal-notify modal-danger modal-xl" role="document">
        <!--Content-->
        <div class="modal-content">
          <!--Header-->
          <div class="modal-header">
            <p class="heading lead">卡片搜索</p>

            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true" class="white-text">&times;</span>
            </button>
          </div>

          <!--Body-->
          <div class="modal-body">
            <div class="left card-filter">
              abc
            </div>
            <div class="right unit-filter">
              <!--标题-->
              <div class="filter-title">
                Unit(蓝底白字 充满一行)
              </div>
              <!--选队伍内容-->
              <div class="unit-content">
                <div v-for="unit in unit_list_new" :key="unit">

                  <div class="unit-all">
                    <input type="checkbox" name="rarity_filter" :value="'unit_'+unit.unit_id"
                           :id="'unit_'+unit.unit_id" class="unit-checkbox">
                    <div class="unit-box">
                      <label :for="'unit_'+unit.unit_id">
                        <img :src="require('../assets/unit_logo_square1/unit_logo_square1_'+unit.unit_id+'.png')"
                             :alt="unit.unit">
                      </label>
                    </div>
                    <div class="chara-box">
                      <div v-for="chara_one in unit.character_list" :key="chara_one">
                        <input v-model="chara_select" type="checkbox" name="chara_filter" :value="chara_one.id"
                               :id="'chara_'+chara_one.id" class="chara-checkbox">
                        <div class="chara-box-one ">
                          <label :for="'chara_'+chara_one.id">
                            <img :src="require('../assets/character_square1/character_square1_'+chara_one.id+'.png')"
                                 :alt="unit.unit">
                          </label>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <input type="checkbox" name="rarity_filter" value="unit_OTHER"
                       id="unit_OTHER" class="unit-checkbox">
                <div class="unit-box">
                  <label for="unit_OTHER">
                    <img :src="require('../assets/unit_logo_square1/unit_logo_square1_OTHER.png')" alt="other">
                  </label>
                </div>
                <div class="clear"></div>
              </div>
              <!--查看已选-->
              <div class="already-select-chara">
                <div v-for="chara in chara_select" :key="chara">
                  <div class="chara-box-one ">
                    <label :for="'chara_'+chara">
                      <img :src="require('../assets/character_square1/character_square1_'+chara+'.png')"
                           :alt="chara">
                    </label>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!--Footer-->
          <div class="modal-footer justify-content-center">
            <a type="button" class="btn btn-danger">Get it now <i class="far fa-gem ml-1 text-white"></i></a>
            <a type="button" class="btn btn-outline-danger waves-effect" data-dismiss="modal">No, thanks</a>
          </div>
        </div>
        <!--/.Content-->
      </div>
    </div>
    <!-- Central Modal Medium Danger-->
  </div>
</template>

<script>
export default {
  name: "SearchQueryWindow",
  data() {
    return {
      chara_select: [],
      unit_list_new: [
        {
          "unit_id": 2,
          "unit": "fine",
          "order": 1,
          "character_list": [
            {"id": 27, "name": "这个"},
            {"id": 22, "name": "这个"},
            {"id": 6, "name": "这个"},
            {"id": 19, "name": "这个"},
          ]
        },
        {
          "unit_id": 1,
          "unit": "trickstar",
          "order": 2,
          "character_list": [
            {"id": 13, "name": "这个"},
            {"id": 12, "name": "这个"},
            {"id": 11, "name": "这个"},
            {"id": 18, "name": "这个"},
          ]
        },
        {
          "unit_id": 5,
          "unit": "ryuseitai",
          "order": 3,
          "character_list": [
            {"id": 28, "name": "这个"},
            {"id": 1, "name": "这个"},
            {"id": 25, "name": "这个"},
            {"id": 7, "name": "这个"},
            {"id": 5, "name": "这个"},
          ]
        },
        {
          "unit_id": 15,
          "unit": "alkaloid",
          "order": 4,
          "character_list": [
            {"id": 69, "name": "这个"},
            {"id": 68, "name": "这个"},
            {"id": 67, "name": "这个"},
            {"id": 70, "name": "这个"},
          ]
        },
        {
          "unit_id": 14,
          "unit": "eden",
          "order": 5,
          "character_list": [
            {"id": 51, "name": "这个"},
            {"id": 50, "name": "这个"},
            {"id": 41, "name": "这个"},
            {"id": 42, "name": "这个"},
          ]
        },
        {
          "unit_id": 9,
          "unit": "valkyrie",
          "order": 6,
          "character_list": [
            {"id": 34, "name": "这个"},
            {"id": 35, "name": "这个"},
          ]
        },
        {
          "unit_id": 7,
          "unit": "2wink",
          "order": 7,
          "character_list": [
            {"id": 8, "name": "这个"},
            {"id": 4, "name": "这个"},
          ]
        },
        {
          "unit_id": 16,
          "unit": "crazyb",
          "order": 8,
          "character_list": [
            {"id": 73, "name": "这个"},
            {"id": 71, "name": "这个"},
            {"id": 72, "name": "这个"},
            {"id": 74, "name": "这个"},
          ]
        },
        {
          "unit_id": 3,
          "unit": "undead",
          "order": 9,
          "character_list": [
            {"id": 15, "name": "这个"},
            {"id": 29, "name": "这个"},
            {"id": 23, "name": "这个"},
            {"id": 16, "name": "这个"},
          ]
        },
        {
          "unit_id": 6,
          "unit": "rabits",
          "order": 10,
          "character_list": [
            {"id": 9, "name": "这个"},
            {"id": 2, "name": "这个"},
            {"id": 30, "name": "这个"},
            {"id": 3, "name": "这个"},
          ]
        },
        {
          "unit_id": 8,
          "unit": "akatsuki",
          "order": 11,
          "character_list": [
            {"id": 26, "name": "这个"},
            {"id": 21, "name": "这个"},
            {"id": 14, "name": "这个"},
          ]
        },
        {
          "unit_id": 4,
          "unit": "knights",
          "order": 12,
          "character_list": [
            {"id": 10, "name": "这个"},
            {"id": 20, "name": "这个"},
            {"id": 33, "name": "这个"},
            {"id": 24, "name": "这个"},
            {"id": 17, "name": "这个"},
          ]
        },
        {
          "unit_id": 10,
          "unit": "switch",
          "order": 13,
          "character_list": [
            {"id": 39, "name": "这个"},
            {"id": 38, "name": "这个"},
            {"id": 37, "name": "这个"},
          ]
        },
        // {
        //   "unit_id": 11,
        //   "unit": "mam",
        //   "order": 14,
        //   "character_list": [
        //     {"id": 40, "name": "这个"},
        //   ]
        // },
        {
          "unit_id": 17,
          "unit": "doubleface",
          "order": 15,
          "character_list": [
            {"id": 40, "name": "这个"},
            {"id": 73, "name": "这个"},
          ]
        }
      ],
    }
  },
  computed: {},
}
</script>

<style scoped>
.modal-header {
  background-color: rgb(8, 25, 73);
  color: white;
  border: 0;
}

.modal-body {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 0;
}

.card-filter, .unit-filter {
  width: 50%;
  padding: 10px;
}

.left.card-filter {
  background-color: rgb(239, 239, 239);

}

.right.unit-filter {
  background-color: rgb(174, 176, 190);
}

.unit-content {
  background-color: rgb(255, 255, 255);
  padding: 5px;
  display: flex;
  flex-direction: column;
  max-height: 500px;
  overflow: auto;
}

.unit-all {
  width: 100%;
}

.clear {
  clear: both;
}

.unit-box {
  background-color: rgb(255, 255, 255);
  width: calc(20% - 14px);
  float: left;
  border: rgb(204, 206, 216) 3px solid;
  border-radius: 10px;
  margin: 7px;
}

.unit-box img {
  width: 100%;
  display: block;
}

.chara-box {
  /*width: calc(100% - 20% + 14px);*/
}

.chara-box-one {
  width: calc(16% - 10px);
  float: left;
  border: rgb(204, 206, 216) 3px solid;
  border-radius: 10px;
  margin: 5px;
}

.chara-box-one img {
  width: 100%;
  display: block;
}

.unit-checkbox, .chara-checkbox {
  display: none;
}

label {
  display: block;
}

.filter-title {
  background-color: rgb(12, 26, 93);
  color: white;
  text-align: left;
  padding: 0 5px;
  font-weight: bolder;
}

input[type=checkbox]:checked + .unit-box {
  border: rgb(35, 61, 195) 3px solid;
  box-shadow: 3px 5px 6px rgba(0, 0, 0, 0.2);
}

input[type=checkbox]:checked + .chara-box-one {
  border: rgb(35, 61, 195) 3px solid;
  box-shadow: 3px 5px 6px rgba(0, 0, 0, 0.2);
}

.already-select-chara .chara-box-one{
  border: rgb(35, 61, 195) 3px solid;
  width: 50px;
}
.already-select-chara{
  overflow-x: scroll;
  display: flex;
  flex-direction: row;
}

</style>