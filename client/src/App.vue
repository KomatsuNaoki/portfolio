<template>
<div id="app">
    <v-app>

        <section class="lo">
            <v-container>
                <v-layout class="header">
                    <v-flex xs12>
                        <h1>KOMATSUBARA TATSUYA</h1>
                    </v-flex>
                </v-layout>

                <v-layout class="body">
                    <v-flex>
                        <router-view />
                    </v-flex>

                </v-layout>

            </v-container>
        </section>
        <footer>
            <a>&copy; 2022 Komatsubara Tatsuya</a>
        </footer>
    </v-app>
</div>
</template>

<!--script>
export default {
    name: 'App',

    data: () => ({
        //
    })
}
</script-->

<style>
.lo {
    display: grid;
    grid:
        "header header header"auto "leftSide body rightSide"1fr "footer footer footer"auto / auto 1fr auto;
    gap: 8px;
}

.container {
    max-width: 100%;
}

.header {
    grid-area: header;
}

#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}

#app h1 {
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
    bottom: 0;
}

footer p {
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
</style>
