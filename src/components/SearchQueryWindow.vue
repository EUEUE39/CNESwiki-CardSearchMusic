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
              <div class="filter-title">
                Unit(蓝底白字 充满一行)
              </div>
              <div class="unit-content">
                <div v-for="unit in unit_list_new" :key="unit">
                  <input type="checkbox" name="rarity_filter" :value="'unit_'+unit.unit_id"
                         :id="'unit_'+unit.unit_id" class="unit-checkbox">
                  <div class="unit-box">
                    <label :for="'unit_'+unit.unit_id">
                      <img :src="require('../assets/unit_logo_square1/unit_logo_square1_'+unit.unit_id+'.png')"
                           :alt="unit.unit">
                    </label>
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
              <div class="longen">
                css3气泡框
              </div>
              <div>
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
      unit_order: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 15],
      unit_list: [
        {
          "unit_id": 2,
          "unit": "fine",
          "unit_name": "fine",
          "tagline": "天上のオーケストラ",
          "unit_desc": "天祥院英智が率いるエレガントユニット。ファンサービスが丁寧で統率の取れたグループ。メディアの露出においてはバラエティ番組は少なめで、トーク番組やイベント司会、ファッションモデルやCMなどのキャンペーンキャラクターなど企業のイメージアップに繋がる仕事が中心的。ユニットのテーマカラーはアイボリー。",
          "image_color": "#ffd7a0",
          "agency": "stapro",
          "order": 1
        },
        {
          "unit_id": 1,
          "unit": "trickstar",
          "unit_name": "Trickstar",
          "tagline": "夜空に煌めくサザンクロス！",
          "unit_desc": "氷鷹北斗が率いる、正統派アイドルユニット。ファンサービスは明るく距離感が近いグループ。和気藹々とした雰囲気と等身大の体当たり精神で、メディア露出においてはバラエティ番組、インタビュアーや司会、ラジオのパーソナリティやCMのキャンペーンキャラクターなどの仕事が中心的。テーマカラーはオレンジ。",
          "image_color": "#ff8b0d",
          "agency": "stapro",
          "order": 2
        },

        {
          "unit_id": 3,
          "unit": "undead",
          "unit_name": "UNDEAD",
          "tagline": "夜闇のワイルドハント",
          "unit_desc": "朔間零が率いるワイルドユニット。ファンサービスは各々で振る舞う自由な気質ではあるものの、柔軟性が高くメディアの露出ではバラエティ番組の司会や、ラジオのパーソナリティ、CMやファッションモデルなどビジュアルとキャラクターを活かした仕事が中心的。テーマカラーは紫。",
          "image_color": "#64368f",
          "agency": "rhylin",
          "order": 9
        },
        {
          "unit_id": 4,
          "unit": "knights",
          "unit_name": "Knights",
          "tagline": "歌を捧げる騎士団",
          "unit_desc": "朱桜司が率いる騎士道ユニット。騎士というキャラクターを活かしてファンサービスが厚いグループ。メディアの露出においてはCMやファッションモデル、バラエティ番組やグルメレポート、ドラマなどビジュアルを活かした仕事が中心的。テーマカラーは紺。",
          "image_color": "#305daa",
          "agency": "newdim",
          "order": 12
        },
        {
          "unit_id": 5,
          "unit": "ryuseitai",
          "unit_name": "流星隊",
          "tagline": "情熱を燃やすヒーローズ☆",
          "unit_desc": "守沢千秋が率いる、正義の戦隊ユニット。ファンサービスが厚く個性の幅が広いグループ。キャラクター性を活かしてメディア露出においては、スポーツも含めたバラエティ番組、グルメレポート、子供番組のメインキャラクターなどの仕事が中心的。ボランティア活動やヒーローショウも学生の時から変わらず、現在も定期的に行われている。テーマカラーはポジションごとの五色。",
          "image_color": "#d8162d",
          "agency": "stapro",
          "order": 3
        },
        {
          "unit_id": 6,
          "unit": "rabits",
          "unit_name": "Ra*bits",
          "tagline": "夢が詰まったおもちゃ箱♪",
          "unit_desc": "真白友也が率いる、ファンシーユニット。ファンサービスは明るく朗らかなグループ。経験は浅いもののフレッシュ感を活かしてメディアの露出においては、CMのキャンペーンキャラクターや街頭レポート、子供番組のキャラクターやナレーションなどクリアな印象に繋がる仕事が中心的。テーマカラーは水色。",
          "image_color": "#68c0f4",
          "agency": "rhylin",
          "order": 10
        },
        {
          "unit_id": 7,
          "unit": "2wink",
          "unit_name": "2wink",
          "tagline": "ふたりでひとつのハッピーメロディ☆",
          "unit_desc": "葵ひなたが率いる、双子のテクノポップユニット。ファンサービスは明るく派手でトリッキーなグループ。臨機応変で柔軟な対応を得意としており、メディアの露出においては、子供番組のキャラクターやバラエティ番組、ライブ中継やイベントの司会など、経験を必要とするキャラクターを活かした仕事が中心的。テーマカラーはネオン。",
          "image_color": "#ff3b9a",
          "agency": "cospro",
          "order": 7
        },
        {
          "unit_id": 8,
          "unit": "akatsuki",
          "unit_name": "紅月",
          "tagline": "堅実、雅に月下の華",
          "unit_desc": "蓮巳敬人が率いる和風ユニット。ファンサービスは控えめで、真面目な気質のため、メディアの露出では情報番組のコメンテーターやラジオ番組のパーソナリティー、ドラマや映画など文化的な仕事が中心的。テーマカラーは赤。",
          "image_color": "#962828",
          "agency": "rhylin",
          "order": 11
        },
        {
          "unit_id": 9,
          "unit": "valkyrie",
          "unit_name": "Valkyrie",
          "tagline": "織りなす芸術のミュージアム",
          "unit_desc": "斎宮宗が率いる、格式高い芸術派ユニット。独自の世界観を持ち、ファンとの接し方も一定の距離感を保つ個性的なグループ。メディアの露出においてはトーク番組のゲストや芸術番組のナレーションや映画、演劇などアーティスト的な側面を活かした仕事が中心的。テーマカラーはワインレッド。",
          "image_color": "#8c2346",
          "agency": "cospro",
          "order": 6
        },
        {
          "unit_id": 10,
          "unit": "switch",
          "unit_name": "Switch",
          "tagline": "解けない幸せのマジカルパーティ",
          "unit_desc": "逆先夏目が率いる、奇抜さを求める魔法使いユニット。ファンに向けて求心力のある世界観とトークを披露するエンターテインメントなグループ。メディアの露出においては、トーク番組のゲスト、コメンテーターやラジオのパーソナリティーなどトークを活かしながらも、子供向けのバラエティ番組やイベント出演など、ショウパフォーマンスを活かした仕事が中心的。テーマカラーは黄緑。",
          "image_color": "#a3ea34",
          "agency": "newdim",
          "order": 13
        },
        {
          "unit_id": 11,
          "unit": "mam",
          "unit_name": "MaM",
          "tagline": "心躍る瞬間を君に！",
          "unit_desc": "三毛縞斑がソロユニットで活動しているユニット。CMなどのキャンペーンキャラクターや、バラエティ番組やグルメレポート、ライブ中継やスポーツバラエティなど司会やアクティブな仕事が中心的。テーマカラーはグレー。",
          "image_color": "#5a6964",
          "agency": "newdim",
          "order": 14
        },
        {
          "unit_id": 14,
          "unit": "eden",
          "unit_name": "Eden",
          "tagline": "心を誘う永遠の楽園",
          "unit_desc": "乱凪砂が率いる、高貴でありながらエネルギッシュなユニット。ファンサービスは求心力のあるトークとドラマチックな演出が派手なグループ。メディアの露出においては、トーク番組のゲストや、CMのキャンペーンキャラクター、ファッションモデルや映画、演劇などビジュアルの煌びやかさを活かした仕事が中心的。テーマカラーは黒。",
          "image_color": "#5f5b5d",
          "agency": "cospro",
          "order": 5
        },
        {
          "unit_id": 15,
          "unit": "alkaloid",
          "unit_name": "ALKALOID",
          "tagline": "貫け、心のスート！",
          "unit_desc": "天城一彩が率いる、スタプロの新星、エッジの利いた音楽隊ユニット。クールで挑戦的な姿勢を取り、ぶつかっていくアグレッシブなグループ。メディアの露出においてはトーク番組やラジオのゲスト、音楽番組のアシスタントやファッションモデルなど宣伝活動を目的とした仕事が中心的。テーマカラーはターコイズ。",
          "image_color": "#2bb7ca",
          "agency": "stapro",
          "order": 4
        },
        {
          "unit_id": 16,
          "unit": "crazyb",
          "unit_name": "Crazy:B",
          "tagline": "飛び回る自由な蜜蜂(ビー)",
          "unit_desc": "天城燐音が率いる、コズプロの新星、エモーショナルなパーティユニット。ファンと一緒に盛り上がるライブ感に特化したグループ。メディアの露出においては、バラエティ番組やトーク番組のゲスト、ラジオのパーソナリティー、CM出演にファッションモデルなど自身を発信する仕事が中心的。テーマカラーはイエロー。",
          "image_color": "#ffd400",
          "agency": "cospro",
          "order": 8
        },
        {
          "unit_id": 17,
          "unit": "doubleface",
          "unit_name": "Double Face",
          "tagline": "双眼のダスティハウンド",
          "unit_desc": "三毛縞斑が率いる、ミステリアスなアンダーグラウンドユニット。世界観を重視した売り出し方で謎のベールを纏いながら、不定期に活動している。メディアの露出においては、雑誌のモデルやCM、ドラマや舞台などビジュアル面をアピールした仕事が中心的。テーマカラーはダークグリーン。",
          "image_color": "#2c4f54",
          "agency": "newdim",
          "order": 15
        }
      ],
      unit_list_new: [
        {
          "unit_id": 2,
          "unit": "fine",
          "order": 1,
        },
        {
          "unit_id": 1,
          "unit": "trickstar",
          "order": 2
        },
        {
          "unit_id": 5,
          "unit": "ryuseitai",
          "order": 3
        },
        {
          "unit_id": 15,
          "unit": "alkaloid",
          "order": 4
        },
        {
          "unit_id": 14,
          "unit": "eden",
          "order": 5
        },
        {
          "unit_id": 9,
          "unit": "valkyrie",
          "order": 6
        },
        {
          "unit_id": 7,
          "unit": "2wink",
          "order": 7
        },
        {
          "unit_id": 16,
          "unit": "crazyb",
          "order": 8
        },
        {
          "unit_id": 3,
          "unit": "undead",
          "order": 9
        },
        {
          "unit_id": 6,
          "unit": "rabits",
          "order": 10
        },
        {
          "unit_id": 8,
          "unit": "akatsuki",
          "order": 11
        },
        {
          "unit_id": 4,
          "unit": "knights",
          "order": 12
        },
        {
          "unit_id": 10,
          "unit": "switch",
          "order": 13
        },
        // {
        //   "unit_id": 11,
        //   "unit": "mam",
        //   "order": 14
        // },
        {
          "unit_id": 17,
          "unit": "doubleface",
          "order": 15
        }
      ],
      unit_to_characters: [
        {
          "id": 1,
          "unit_id": 1,
          "character_id": 13,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.035+09:00",
          "updated_at": "2020-07-15T13:17:28.293+09:00",
          "order_num_in_unit_as_list": 3
        },
        {
          "id": 2,
          "unit_id": 1,
          "character_id": 12,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.038+09:00",
          "updated_at": "2020-07-15T13:17:28.301+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 3,
          "unit_id": 1,
          "character_id": 11,
          "order_num_in_unit": 3,
          "created_at": "2020-03-15T12:42:24.042+09:00",
          "updated_at": "2020-07-15T13:17:28.308+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 4,
          "unit_id": 1,
          "character_id": 18,
          "order_num_in_unit": 4,
          "created_at": "2020-03-15T12:42:24.047+09:00",
          "updated_at": "2020-07-15T13:17:28.313+09:00",
          "order_num_in_unit_as_list": 4
        },
        {
          "id": 5,
          "unit_id": 2,
          "character_id": 27,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.051+09:00",
          "updated_at": "2020-07-15T13:17:28.319+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 6,
          "unit_id": 2,
          "character_id": 22,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.055+09:00",
          "updated_at": "2020-07-15T13:17:28.325+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 7,
          "unit_id": 2,
          "character_id": 6,
          "order_num_in_unit": 3,
          "created_at": "2020-03-15T12:42:24.059+09:00",
          "updated_at": "2020-07-15T13:17:28.333+09:00",
          "order_num_in_unit_as_list": 3
        },
        {
          "id": 8,
          "unit_id": 2,
          "character_id": 19,
          "order_num_in_unit": 4,
          "created_at": "2020-03-15T12:42:24.062+09:00",
          "updated_at": "2020-07-15T13:17:28.339+09:00",
          "order_num_in_unit_as_list": 4
        },
        {
          "id": 9,
          "unit_id": 3,
          "character_id": 15,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.066+09:00",
          "updated_at": "2020-07-15T13:17:28.345+09:00",
          "order_num_in_unit_as_list": 4
        },
        {
          "id": 10,
          "unit_id": 3,
          "character_id": 29,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.070+09:00",
          "updated_at": "2020-07-15T13:17:28.352+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 11,
          "unit_id": 3,
          "character_id": 23,
          "order_num_in_unit": 3,
          "created_at": "2020-03-15T12:42:24.074+09:00",
          "updated_at": "2020-07-15T13:17:28.359+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 12,
          "unit_id": 3,
          "character_id": 16,
          "order_num_in_unit": 4,
          "created_at": "2020-03-15T12:42:24.078+09:00",
          "updated_at": "2020-07-15T13:17:28.364+09:00",
          "order_num_in_unit_as_list": 3
        },
        {
          "id": 13,
          "unit_id": 4,
          "character_id": 10,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.082+09:00",
          "updated_at": "2020-07-15T13:17:28.371+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 14,
          "unit_id": 4,
          "character_id": 20,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.086+09:00",
          "updated_at": "2020-07-15T13:17:28.377+09:00",
          "order_num_in_unit_as_list": 5
        },
        {
          "id": 15,
          "unit_id": 4,
          "character_id": 33,
          "order_num_in_unit": 3,
          "created_at": "2020-03-15T12:42:24.090+09:00",
          "updated_at": "2020-07-15T13:17:28.384+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 16,
          "unit_id": 4,
          "character_id": 24,
          "order_num_in_unit": 4,
          "created_at": "2020-03-15T12:42:24.094+09:00",
          "updated_at": "2020-07-15T13:17:28.391+09:00",
          "order_num_in_unit_as_list": 3
        },
        {
          "id": 17,
          "unit_id": 4,
          "character_id": 17,
          "order_num_in_unit": 5,
          "created_at": "2020-03-15T12:42:24.097+09:00",
          "updated_at": "2020-07-15T13:17:28.396+09:00",
          "order_num_in_unit_as_list": 4
        },
        {
          "id": 18,
          "unit_id": 5,
          "character_id": 28,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.101+09:00",
          "updated_at": "2020-07-15T13:17:28.402+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 19,
          "unit_id": 5,
          "character_id": 1,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.106+09:00",
          "updated_at": "2020-07-15T13:17:28.408+09:00",
          "order_num_in_unit_as_list": 3
        },
        {
          "id": 20,
          "unit_id": 5,
          "character_id": 25,
          "order_num_in_unit": 3,
          "created_at": "2020-03-15T12:42:24.110+09:00",
          "updated_at": "2020-07-15T13:17:28.415+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 21,
          "unit_id": 5,
          "character_id": 7,
          "order_num_in_unit": 4,
          "created_at": "2020-03-15T12:42:24.114+09:00",
          "updated_at": "2020-07-15T13:17:28.422+09:00",
          "order_num_in_unit_as_list": 5
        },
        {
          "id": 22,
          "unit_id": 5,
          "character_id": 5,
          "order_num_in_unit": 5,
          "created_at": "2020-03-15T12:42:24.118+09:00",
          "updated_at": "2020-07-15T13:17:28.426+09:00",
          "order_num_in_unit_as_list": 4
        },
        {
          "id": 23,
          "unit_id": 6,
          "character_id": 9,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.122+09:00",
          "updated_at": "2020-07-15T13:17:28.433+09:00",
          "order_num_in_unit_as_list": 3
        },
        {
          "id": 24,
          "unit_id": 6,
          "character_id": 2,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.126+09:00",
          "updated_at": "2020-07-15T13:17:28.440+09:00",
          "order_num_in_unit_as_list": 4
        },
        {
          "id": 25,
          "unit_id": 6,
          "character_id": 30,
          "order_num_in_unit": 3,
          "created_at": "2020-03-15T12:42:24.130+09:00",
          "updated_at": "2020-07-15T13:17:28.445+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 26,
          "unit_id": 6,
          "character_id": 3,
          "order_num_in_unit": 4,
          "created_at": "2020-03-15T12:42:24.134+09:00",
          "updated_at": "2020-07-15T13:17:28.451+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 27,
          "unit_id": 7,
          "character_id": 8,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.138+09:00",
          "updated_at": "2020-07-15T13:17:28.458+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 28,
          "unit_id": 7,
          "character_id": 4,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.142+09:00",
          "updated_at": "2020-07-15T13:17:28.466+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 29,
          "unit_id": 8,
          "character_id": 26,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.146+09:00",
          "updated_at": "2020-07-15T13:17:28.473+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 30,
          "unit_id": 8,
          "character_id": 21,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.150+09:00",
          "updated_at": "2020-07-15T13:17:28.478+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 31,
          "unit_id": 8,
          "character_id": 14,
          "order_num_in_unit": 3,
          "created_at": "2020-03-15T12:42:24.154+09:00",
          "updated_at": "2020-07-15T13:17:28.483+09:00",
          "order_num_in_unit_as_list": 3
        },
        {
          "id": 32,
          "unit_id": 9,
          "character_id": 34,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.157+09:00",
          "updated_at": "2020-07-15T13:17:28.488+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 33,
          "unit_id": 9,
          "character_id": 35,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.161+09:00",
          "updated_at": "2020-07-15T13:17:28.494+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 34,
          "unit_id": 10,
          "character_id": 39,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.165+09:00",
          "updated_at": "2020-07-15T13:17:28.501+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 35,
          "unit_id": 10,
          "character_id": 38,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.169+09:00",
          "updated_at": "2020-07-15T13:17:28.505+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 36,
          "unit_id": 10,
          "character_id": 37,
          "order_num_in_unit": 3,
          "created_at": "2020-03-15T12:42:24.173+09:00",
          "updated_at": "2020-07-15T13:17:28.510+09:00",
          "order_num_in_unit_as_list": 3
        },
        {
          "id": 37,
          "unit_id": 11,
          "character_id": 40,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.176+09:00",
          "updated_at": "2020-07-15T13:17:28.516+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 38,
          "unit_id": 14,
          "character_id": 51,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.180+09:00",
          "updated_at": "2020-07-15T13:17:28.521+09:00",
          "order_num_in_unit_as_list": 3
        },
        {
          "id": 39,
          "unit_id": 14,
          "character_id": 50,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.184+09:00",
          "updated_at": "2020-07-15T13:17:28.549+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 40,
          "unit_id": 14,
          "character_id": 41,
          "order_num_in_unit": 3,
          "created_at": "2020-03-15T12:42:24.188+09:00",
          "updated_at": "2020-07-15T13:17:28.555+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 41,
          "unit_id": 14,
          "character_id": 42,
          "order_num_in_unit": 4,
          "created_at": "2020-03-15T12:42:24.191+09:00",
          "updated_at": "2020-07-15T13:17:28.561+09:00",
          "order_num_in_unit_as_list": 4
        },
        {
          "id": 42,
          "unit_id": 15,
          "character_id": 69,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.195+09:00",
          "updated_at": "2020-07-15T13:17:28.567+09:00",
          "order_num_in_unit_as_list": 3
        },
        {
          "id": 43,
          "unit_id": 15,
          "character_id": 68,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.199+09:00",
          "updated_at": "2020-07-15T13:17:28.573+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 44,
          "unit_id": 15,
          "character_id": 67,
          "order_num_in_unit": 3,
          "created_at": "2020-03-15T12:42:24.202+09:00",
          "updated_at": "2020-07-15T13:17:28.579+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 45,
          "unit_id": 15,
          "character_id": 70,
          "order_num_in_unit": 4,
          "created_at": "2020-03-15T12:42:24.206+09:00",
          "updated_at": "2020-07-15T13:17:28.584+09:00",
          "order_num_in_unit_as_list": 4
        },
        {
          "id": 46,
          "unit_id": 16,
          "character_id": 73,
          "order_num_in_unit": 1,
          "created_at": "2020-03-15T12:42:24.210+09:00",
          "updated_at": "2020-07-15T13:17:28.591+09:00",
          "order_num_in_unit_as_list": 3
        },
        {
          "id": 47,
          "unit_id": 16,
          "character_id": 71,
          "order_num_in_unit": 2,
          "created_at": "2020-03-15T12:42:24.213+09:00",
          "updated_at": "2020-07-15T13:17:28.598+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 48,
          "unit_id": 16,
          "character_id": 72,
          "order_num_in_unit": 3,
          "created_at": "2020-03-15T12:42:24.217+09:00",
          "updated_at": "2020-07-15T13:17:28.603+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 49,
          "unit_id": 16,
          "character_id": 74,
          "order_num_in_unit": 4,
          "created_at": "2020-03-15T12:42:24.221+09:00",
          "updated_at": "2020-07-15T13:17:28.611+09:00",
          "order_num_in_unit_as_list": 4
        },
        {
          "id": 52,
          "unit_id": 17,
          "character_id": 40,
          "order_num_in_unit": 1,
          "created_at": "2020-08-10T13:31:07.872+09:00",
          "updated_at": "2020-08-10T13:31:07.872+09:00",
          "order_num_in_unit_as_list": 1
        },
        {
          "id": 53,
          "unit_id": 17,
          "character_id": 73,
          "order_num_in_unit": 2,
          "created_at": "2020-08-10T13:31:07.879+09:00",
          "updated_at": "2020-08-10T13:31:07.879+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 51,
          "unit_id": 18,
          "character_id": 32,
          "order_num_in_unit": 1,
          "created_at": "2020-03-31T14:35:45.963+09:00",
          "updated_at": "2020-07-15T13:17:28.622+09:00",
          "order_num_in_unit_as_list": 2
        },
        {
          "id": 50,
          "unit_id": 18,
          "character_id": 31,
          "order_num_in_unit": 2,
          "created_at": "2020-03-31T14:35:45.958+09:00",
          "updated_at": "2020-07-15T13:17:28.616+09:00",
          "order_num_in_unit_as_list": 1
        }
      ]
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

.unit-content{
  background-color: rgb(255,255,255);
}
/*.unit-content:after{*/
/*  !*background-color:blue;*!*/
/*  !*float:left;*!*/
/*  content:"";*/
/*  !*display: block;*!*/
/*  clear: both;*/
/*}*/
.clear{
  clear:both;
}

.unit-box {
  background-color: rgb(255, 255, 255);
  width: calc(20% - 10px);
  float: left;
  border: rgb(204, 206, 216) 3px solid;
  border-radius: 10px;
  margin: 5px;
}

.unit-box img {
  width: 100%;
  display: block;
}

.unit-checkbox{
  display: none;
}
label{
  display: block;
}

.filter-title{
  background-color:rgb(12,26,93);
  color: white;
  text-align: left;
  padding: 0 5px;
  font-weight: bolder;
}

input[type=checkbox]:checked + .unit-box{
  border: rgb(35,61,195) 3px solid;
  box-shadow: 3px 5px 6px rgba(0, 0, 0, 0.2);
}

.longen {
  width: 300px;
  height: 100px;
  border: 5px solid #09F;
  position: relative;
  background-color: #FFF;
  margin:33px 0 0 0;
}

.longen:before,
.longen:after {
  content: "";
  display: block;
  border-width: 20px;
  position: absolute;
  top: -40px;
  left: 100px;
  border-style: dashed dashed solid;
  border-color: transparent transparent #09F;
  font-size: 0;
  line-height: 0;
}

.longen:after {
  top: -33px;
  border-color: transparent transparent #FFF;
}
</style>