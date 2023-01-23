<template>
<div id="app">

<section class="layout">
    <div class="header">
        <p>KOMATSUBARA TATSUYA</p>
    </div>
    <div class="leftSide">
        <nav>
            <router-link to="/">Home</router-link>
            <router-link to="/about">About</router-link>
        </nav>
    </div>
    <div class="body">

    <router-view />
    </div>
    <div class="rightSide">4</div>
    <div class="footer">5</div>
</section>

    <footer>
        <a>&copy; 2022 Komatsubara Tatsuya</a>
    </footer>
</div>
</template>

<style>

.layout {
    width: 1366px;
    height: 768px;

    display: grid;
    grid:
    "header header header" auto
    "leftSide body rightSide" 1fr
    "footer footer footer" auto
    / auto 1fr auto;
    gap: 8px;
}

.header { grid-area: header; }
.leftSide { grid-area: leftSide; }
.body { grid-area: body; }
.rightSide { grid-area: rightSide; }
.footer { grid-area: footer; }

#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}

#app p {
    text-align: left;
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
