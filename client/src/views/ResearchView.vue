<template>
  <v-container>
    <div class="research">
        <div class="content">
          <div class="my-4">
            <div class="Rtitle" style="font-weight:bold;font-size:18px;padding:5px;">
              {{title[myCarousel]}}
            </div>
            <v-carousel v-model="myCarousel"
            height="auto"
            width="auto"
            style="display:inline-block;width:100%;aspect-ratio:16/9;max-width:800px;max-height:450px;">
              <v-carousel-item
                src="../assets/RS_0.png"
                cover
              ></v-carousel-item>
              <v-carousel-item
                src="../assets/RS_1.png"
                cover
              ></v-carousel-item>
              <v-carousel-item
                src="../assets/RS_2.png"
                cover
              ></v-carousel-item>
            </v-carousel>
            </div>
            <div class="caption">
              <h3>{{cap[myCarousel]}}</h3>
              <br>
              <br>
              <a :href="lnk[myCarousel]">{{ach[myCarousel]}}</a>
            </div>
        </div>
    </div>
  </v-container>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'ResearchView',
  components: {

  },
  data () {
    return {
      title: ['優柔不断な選択者を後押しするメガネ', 'mureQ', 'Okidoki'],
      cap: ['選択中の視線運動を計測し、それに基づいた興味推定・推薦をメガネ型デバイスが行うことで、優柔不断な人の選択を支援する研究。',
        'ユーザの持つユニークな音楽ニーズに対して、集合知で楽曲を集め、プレイリストを生成するWebサービス。',
        'アラームを止めるために友人間で競い合うミニゲームをクリアする仕組みを取り入れ、寝坊を防止するスマホアプリ。'],
      lnk: ['https://dl.nkmr-lab.org/papers/396',
        'https://dl.nkmr-lab.org/papers/327',
        'http://contest2022.sig-cds.net/'],
      ach: ['小松原 達哉, 中村 聡史. 優柔不断な選択者を後押しする眼鏡型デバイスの実現とその評価, 情報処理学会 研究報告ヒューマンコンピュータインタラクション（HCI）, Vol.2022-HCI-199, No.8, pp.1-7, 2022.\n小松原達哉, 中村聡史. 視線計測による興味推定を用いた優柔不断な選択者を後押しするシステムの提案, 第14回データ工学と情報マネジメントに関するフォーラム, 2022.',
        '小松原 達哉, 松山 直人, 野中 滉介, 二宮 洸太, 斉藤 絢基, 中村 聡史. 集合知を利用した音楽キュレーションサービスの実装とその分析, 情報処理学会 研究報告エンタテインメントコンピューティング（EC）, Vol.2021-EC-59, No.28, pp.1-8, 2021.',
        '第10回 学生スマートフォンアプリコンテスト 奨励賞受賞']
    }
  },
  setup () {
    const myCarousel = ref(0)
    const myCarouselControl = () => {
      myCarousel.value = myCarousel.value + 1
      if (myCarousel.value >= 3) {
        myCarousel.value = 0
      }
    }
    return {
      myCarousel,
      myCarouselControl
    }
  },
  mounted: function () {
    /*
    v-carousel-item.addEventListener('click', function () {
      console.log('wao')
    }) */
  }
}
</script>

<style>

.my-4{
  width: 100%;
}

.caption{
  background-color: rgba(255,255,255,0.7);
  margin: 5px;
  padding:5px;
}

</style>
