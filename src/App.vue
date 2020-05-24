<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <router-view />
  </div>
</template>

<style lang="scss">
html {
  width: 100vw;
  height: 100vh;
  background: linear-gradient(
    0.4turn,
    #d89adb,
    #dfa5cd,
    #e4b0bd,
    #c48bcf,
    #9352f6
  );
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  box-sizing: border-box;
  height: 5%;
  width: 100vw;
  left: 0;
  top: 0;
  position: absolute;
  padding: 14px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
