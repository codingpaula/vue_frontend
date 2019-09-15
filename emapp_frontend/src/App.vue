<template>
  <div id="app">
    <b-navbar type="dark" variant="dark" id="nav" sticky>
      <b-navbar-brand>
        <router-link to="/">
          <img src="@/assets/Icon01-180.png" class="brand-img" /> EMAPP
        </router-link>
      </b-navbar-brand>
      <router-link to="/about">About</router-link>
      <router-link to="/history">History</router-link>
    </b-navbar>
    <router-view />
    <div id="footer" class="fixed-bottom">
      <router-link to="/impressum">Impressum</router-link>
    </div>
  </div>
</template>

<script></script>

<style lang="scss">
html, body {
  height: 100vh;
}
#app {
  display: flex;
  flex-direction: column;
  height: 100vh;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 1rem;
  a {
    padding-left: 0.5rem;
    padding-right: 0.5rem;
    font-weight: bold;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
#footer {
  background-color: #343A40;
  padding-top: 1rem;
  padding-bottom: 1rem;
}
.brand-img {
  height: 50px;
  padding-right: 1rem;
}
</style>
