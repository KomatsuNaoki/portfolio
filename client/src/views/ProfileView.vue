<template>
    <v-container>
    <div class="profile">
        <div class="content">
            <img src="../assets/profile.jpg"
            />
            <v-row
            justify="center"
            width="100%"
            v-for="(mPU, index) in title"
            :key="index"

            >
                <about-box :title="title[index]" :text="text[index]"></about-box>
            </v-row>
        </div>
    </div>
</v-container>
</template>

<script>
import AboutBox from '../components/AboutBox'
export default {
  name: 'ProfileView',
  components: {
    AboutBox
  },
  data () {
    return {
      page: 'Profile',
      title: ['氏名', '所属', '経歴', '趣味', 'スキル'],
      text: ['小松原 達哉\nKomatsubara Tatsuya',
        '明治大学大学院　先端数理科学研究科\n先端メディアサイエンス専攻 1年\n中村研究室',
        '2022年 3月\n明治大学 総合数理学部\n先端メディアサイエンス学科 卒業',
        '写真撮影 音楽鑑賞\n3Dモデリング ゲーム',
        'Processing Javascript\nBlender(趣味レベル) 画像加工ソフト']
    }
  }
}
</script>

<style>

.profile {
    height: 100%;
}

.profile .content {
    padding: 10px;
    width:100%;
    height: 100%;
    position: absolute;          /* 位置指定 */
    top: 50%;                    /* 親要素の半分下にずらす */
    left: 50%;                   /* 親要素の半分右にずらす */
    transform: translateY(-50%) translateX(-50%);    /* 要素自体の半分、上と左にずらす */
    overflow-y: auto;
    overflow-x:hidden;
    padding: 1px;
}

img {
    width:70%;
    max-width: 200px;
    margin:"10px"
}

</style>
