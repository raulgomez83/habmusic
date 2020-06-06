<template>
  <div id="app">
    <h1>🧟‍♀️🍄 H Radio 🍄👽</h1>
    <div id="nav">
      <router-link to="/">Home</router-link>|
      <router-link to="/top-tracks">Toptracks</router-link>|
      <router-link to="/top-artists">Topartists</router-link>|
      <router-link to="/about">About</router-link>
    </div>
    <router-view />
  </div>
</template>

<style>
* {
  margin: 0 auto;
  padding: 0;
  background-color: purple;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: gold;
}

#nav {
  padding: 30px;
}

a {
  font-weight: bold;
  color: gold;
  text-decoration: none;
}

a.router-link-exact-active {
  color: pink;
}
h1 {
  color: gold;
  text-shadow: 2px 2px lime;
}
ul {
  list-style: none;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  background: pink;
}
li {
  color: gold;
  margin: 0.5rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-size: 1.1rem;
  font-weight: bold;
}
</style>
