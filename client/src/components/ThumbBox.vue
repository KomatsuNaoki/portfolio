<template>
    <div class="box">
        <a>
            {{ title }}
        </a>
        <div class="thumb">
            <a :href="link">
            <img v-bind:src="thumbPhoto" :href="link"/>
        </a>
        </div>
    </div>
</template>

<script>
export default {
  name: 'ThumbBox',
  props: ['title', 'thumbPhoto', 'link']
}

</script>

<style>

.box {
    padding: 15px;
    max-width: 400px;
    width: 100%;
}

.box a{
    color: black;
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

</style>
