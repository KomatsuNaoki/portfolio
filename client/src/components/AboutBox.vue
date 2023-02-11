<template>
    <div class="about">
        <a>
            {{ title }}
        </a>
        <div class="textbox">
            <h4>
                {{ text }}
            </h4>
        </div>
    </div>
</template>

<script>
export default {
  name: 'AboutBox',
  props: ['title', 'text']
}
</script>

<style>

.about a{
    color: black;
    text-align: center;
    font-size: large;
}

.textbox{
    background-color: rgba(255,255,255,0.5);
}

.textbox h4{
    text-align: center;
    font-size: larger;
}

</style>
