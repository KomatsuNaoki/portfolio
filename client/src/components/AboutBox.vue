<template>
    <div class="about">
        <h3>
            {{ title }}
        </h3>
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

.about {
    padding: 15px;
    max-width: 400px;
    width: 100%;
}

.about h3{
    width: auto;
    padding: 5px;
    font-family: Noto Sans JP;
    font-weight: bold;
    background-color: #394f6a;
    color: #ddd;
    text-align: center;
    font-size: large;
}

.textbox{
    background-color: rgba(255,255,255,0.7);
    margin: 5px;
}

.textbox h4{
    color: #394f6a;
    text-align: center;
    font-size: larger;
    white-space: pre-wrap;
}

</style>
