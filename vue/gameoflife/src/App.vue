<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgb(120, 115, 115);
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: pink;
}

nav a.router-link-exact-active {
  color: rgb(245, 92, 117);
}
</style>
