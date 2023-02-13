<template>
    <div class="box">
        <h9>
            {{ title }}
        </h9>
        <div class="thumb">
            <a :href="link">
            <img :src="imgSrc">
        </a>
        </div>
    </div>
</template>

<script>
export default {
  name: 'ThumbBox',
  props: ['title', 'thumbPhoto', 'link'],
  data () {
    return {
      imgSrc: require('../assets/' + this.thumbPhoto + '.jpg')
    }
  },
  conmputed: {
    imgSrc: function () {
      // return require('../assets/' + this.thumbPhoto + '.jpg')
      return require('../assets/profile.jpg')
    }
  },
  mounted: function () {
    console.log(this.thumbPhoto)
    console.log(this.imgSrc)
  }
}

</script>

<style>

.box {
    padding: 15px;
    max-width: 400px;
    width: 100%;
}

.box h9{
    padding: 5px;
    font-family: Noto Sans JP;
    font-weight: bold;
    background-color: #394f6a;
    color: #ddd;
    text-align: center;
    font-size: large;
}

.textbox{
    background-color: rgba(255,255,255,0.5);
    padding: 5px;
}

.textbox h4{
    text-align: center;
    font-size: larger;
    white-space: pre-wrap;
}

.thumb img{
    margin: 10px;
    -webkit-transition: -webkit-transform 0.15s linear;
    -moz-transition: -moz-transform 0.15s linear;
    -o-transition: -o-transform 0.15s linear;
    -ms-transition: -ms-transform 0.15s linear;
    transition: transform 0.15s linear;
    box-shadow: 0 10px 25px 0 rgba(0, 0, 0, .7);
}

.thumb img:hover{
    -webkit-transform: scale(1.1);
    -moz-transform: scale(1.1);
    -o-transform: scale(1.1);
    -ms-transform: scale(1.1);
    transform: scale(1.1);
}

</style>
