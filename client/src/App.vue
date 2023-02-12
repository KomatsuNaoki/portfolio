<template>
<div id="app">
    <v-app>
        <v-layout class="header">
            <v-flex xs12>
                <h1>KOMATSUBARA TATSUYA</h1>
                <!--p>{{page}}</p-->
            </v-flex>
        </v-layout>

        <v-container>
        <section class="lo">
            <router-view />
        </section>
        <footer>
            <a>&copy; 2022 Komatsubara Tatsuya</a>
        </footer>
    </v-container>
    </v-app>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      page: 'Home'
    }
  },
  methods: {
    goHome () {
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
}

.header {
    background-color: rgba(255,255,255,0.5);
    width: 100%;
    grid-area: header;
    position: fixed;          /* 位置指定 */
}

.flex xs12{
    display: flex;
}

p {
    text-align: right;
    font-size: 20px;
    margin:13px;
    position: static;
    top: 13px;                    /* 親要素の半分下にずらす */
    right: 13px;                   /* 親要素の半分右にずらす */
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
    background-position: center center;
    background-attachment: fixed;
}

.lo{
    width: 100%;
    height: calc(100% - 110px);
    position: absolute;          /* 位置指定 */
    top: 50%;                    /* 親要素の半分下にずらす */
    left: 50%;                   /* 親要素の半分右にずらす */
    transform: translateY(-50%) translateX(-50%);    /* 要素自体の半分、上と左にずらす */
}

#app h1 {
    margin:10px;
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
    float: left;
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
    width: 100%;
    height: 50px;
    bottom: 0;
    text-align: center;
    position: fixed;
}

footer a {
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

.home .content{
    position: absolute;          /* 位置指定 */
    top: 50%;                    /* 親要素の半分下にずらす */
    left: 50%;                   /* 親要素の半分右にずらす */
    transform: translateY(-50%) translateX(-50%);    /* 要素自体の半分、上と左にずらす */
    overflow-y: auto;
    overflow-x:hidden;
    padding: 1px;
}

</style>
