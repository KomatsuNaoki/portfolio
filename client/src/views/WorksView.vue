<template>
<div class="works">
    <div class="content">
        <v-row
            justify="center"
            width="100%"
            margin="1px"
            v-for="(mPU, index) in title"
            :key="index"
            >
            <thumb-box :title="title[index]" :thumbPhoto="thumbnail[index]" :link="link[index]"></thumb-box>
        </v-row>
    </div>
</div>
</template>

<script>
import ThumbBox from '../components/ThumbBox'
export default {
  name: 'WorksView',
  components: {
    ThumbBox
  },
  data () {
    return {
      title: ['研究', '趣味'],
      thumbnail: ['researchThumbnail', 'galleryThumbnail'],
      link: ['#/research', '#/gallery']
    }
  }
}
</script>

<style>

.works {
    height: 100%;
}

.works .content{
    width: 100%;
    height: auto;
    text-align: center;
    position: absolute;          /* 位置指定 */
    top: 50%;                    /* 親要素の半分下にずらす */
    left: 50%;                   /* 親要素の半分右にずらす */
    transform: translateY(-50%) translateX(-50%);    /* 要素自体の半分、上と左にずらす */
    overflow-y: auto;
    overflow-x:hidden;
    /*padding: 1px;*/
}

.works .content .row{
  margin: 1px;
}

.ma-5 {
    text-align: center;
}

img {
  width:80%;
  max-width: 700px;
  margin:"10px";

}

</style>
