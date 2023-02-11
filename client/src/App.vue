<template>
<div id="app">
    <v-app>
        <v-layout class="header">
            <v-flex xs12>
                <h1  @click="goHome()">KOMATSUBARA TATSUYA</h1>
            </v-flex>
        </v-layout>

        <section class="lo">
            <v-container>
                    <router-view />
            </v-container>
        </section>
        <footer>
            <a>&copy; 2022 Komatsubara Tatsuya</a>
        </footer>
    </v-app>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {
    goHome () {
      console.log('hello')
      this.$router.push('/')
    }
  }
}
</script>

<style>
/*
.lo {
    display: grid;
    grid:
        "header header header"auto "leftSide body rightSide"1fr "footer footer footer"auto / auto 1fr auto;
    gap: 8px;
}*/

.container {
    max-width: 100%;
    height: 100%;
}

.header {
    background-color: rgba(255,255,255,0.5);
    width: 100%;
    height: 30px;
    grid-area: header;
    position: absolute;          /* 位置指定 */
}

.app{
    display: block;
}

#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    background: url("~@/assets/home.png") center center;
    background-repeat: no-repeat;
    background-size: auto 100%;
    background-attachment: fixed;
    overflow: hidden;
}

.lo{
    width: 100%;
    height: calc(100% - 60px);
    position: absolute;          /* 位置指定 */
    top: 50%;                    /* 親要素の半分下にずらす */
    left: 50%;                   /* 親要素の半分右にずらす */
    transform: translateY(-50%) translateX(-50%);    /* 要素自体の半分、上と左にずらす */
}

#app h1 {
    position: static;
    top: 10px;                    /* 親要素の半分下にずらす */
    left: 10px;                   /* 親要素の半分右にずらす */
    text-align: left;
    color: #fff;
    font-family: Inter, Impact, Arial, sans-serif;
    font-weight: bold;
    font-size: 20px;
    -webkit-text-stroke: 0.5px black;
    text-shadow: 2px 2px 3px #76FF03;
}

#app h2 {
    color: #fff;
    font-family: Inter, Impact, Arial, sans-serif;
    font-weight: bold;
    font-size: 20px;
    -webkit-text-stroke: 0.5px black;
    text-shadow: 2px 2px 3px #76FF03;
}

footer {
    position: fixed;
    width: 100%;
    height: 30px;
    bottom: 0;
}

footer p {
    color: #2c3e50;
    font-family: Impact, Arial, sans-serif;
    font-weight: bold;
}

nav {
    padding: 30px;
}

nav a {
    font-weight: bold;
    color: #2c3e50;
}

nav a.router-link-exact-active {
    color: #42b983;
}

.content{
    position: absolute;          /* 位置指定 */
    top: 50%;                    /* 親要素の半分下にずらす */
    left: 50%;                   /* 親要素の半分右にずらす */
    transform: translateY(-50%) translateX(-50%);    /* 要素自体の半分、上と左にずらす */
}

</style>
