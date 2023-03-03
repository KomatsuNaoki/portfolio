<template>
  <div class="photo">
    <ul class="gallery">
        <li><img src="../assets/photos/01.jpg" alt=""></li>
        <li><img src="../assets/photos/02.jpg" alt=""></li>
        <li><img src="../assets/photos/03.jpg" alt=""></li>
        <li><img src="../assets/photos/04.jpg" alt=""></li>
        <li><img src="../assets/photos/05.jpg" alt=""></li>
        <li><img src="../assets/photos/06.jpg" alt=""></li>
        <li><img src="../assets/photos/07.jpg" alt=""></li>
        <li><img src="../assets/photos/08.jpg" alt=""></li>
        <li><img src="../assets/photos/09.jpg" alt=""></li>
        <li><img src="../assets/photos/10.jpg" alt=""></li>
        <li><img src="../assets/photos/11.jpg" alt=""></li>
        <li><img src="../assets/photos/12.jpg" alt=""></li>
        <li><img src="../assets/photos/13.jpg" alt=""></li>
        <li><img src="../assets/photos/14.jpg" alt=""></li>
        <li><img src="../assets/photos/15.jpg" alt=""></li>
    </ul>
  </div>
</template>

<script src="https://code.jquery.com/jquery-3.4.1.min.js" integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo=" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.10.0/js/lightbox.min.js"></script>

<script>
export default {

}
</script>

<style>

.v-application ul {
    padding-right: 24px;
}

.photo{
    padding: 10px;
    width:100%;
    height: 100%;
    position: absolute;          /* 位置指定 */
    top: 50%;                    /* 親要素の半分下にずらす */
    left: 50%;                   /* 親要素の半分右にずらす */
    transform: translateY(-50%) translateX(-50%);    /* 要素自体の半分、上と左にずらす */
    overflow-y: auto;
    overflow-x: hidden;
    padding: 1px;
}

.gallery{
    columns: 4;/*段組みの数*/
    padding:0 15px;/*ギャラリー左右に余白をつける*/
    margin:0;
}

.gallery li {
    margin-bottom: 20px;/*各画像下に余白をつける*/
    list-style:none;
}

    /*ギャラリー内のイメージは横幅100%にする*/
.gallery img{
    width:100%;
    height:auto;
    vertical-align: bottom;/*画像の下にできる余白を削除*/
}

    /*横幅900px以下の段組み設定*/
@media only screen and (max-width: 900px) {
    .gallery{
        columns:3;
    }
}

@media only screen and (max-width: 768px) {
    .gallery{
        columns: 2;
    }
}
</style>
