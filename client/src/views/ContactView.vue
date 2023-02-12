<template>
    <div class="contact">
        <div class="content">
            <div class="address">
                <h5>連絡先はこちら</h5>
                <h6>cs222019[at]meiji.ac.jp</h6>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'ContactView',

  components: {
  }
}
</script>

<style>

.contact {
    width: 100%;
}

.contact .content{
    width: 100%;
    height: 100%;
}

.address {
    padding: 10px;
    position: absolute;          /* 位置指定 */
    top: 50%;                    /* 親要素の半分下にずらす */
    left: 50%;                   /* 親要素の半分右にずらす */
    transform: translateY(-50%) translateX(-50%);    /* 要素自体の半分、上と左にずらす */
    background-color: rgba(255, 255, 255, 0.5);
}

h5 {
    font-size: 15px;
}

h6 {
    font-size: 20px;
}

</style>
