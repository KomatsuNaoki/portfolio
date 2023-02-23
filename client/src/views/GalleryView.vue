
<script src="https://snapwidget.com/js/snapwidget.js"></script>

<template>
  <!-- SnapWidget -->
  <div class="insta">
    <iframe src="https://snapwidget.com/embed/1024731" class="snapwidget-widget" allowtransparency="true" frameborder="0" scrolling="no"></iframe>
  </div>
</template>

<script>
export default {

  name: 'GalleryView',
  components: {

  }
}
</script>

<style>

.insta {
    height:100%;
    max-height: 400px;
    margin:"10px";
}

iframe{
    border:none;
    width:80%;
    max-width:400px;
    height:300px;
}

</style>
