<template>
  <div id="app">
    <div id="nav">
      <router-link class="navigation" to="/">Home</router-link>
      <router-link class="navigation" to="/about">About</router-link>
    </div>
    <router-view />
  </div>
</template>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  color: #2c3e50;
  width: 80%;
  margin: auto;
  font-size: 20px;
}

.button {
  display: inline-block;
  border: none;
  background: #555;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
}

.button:hover {
  background: #666;
}

#nav {
  text-align: center;
  margin: 15px;
  justify-content: space-between;
}
.navigation {
  text-decoration: none;
  margin-left: 30px;
}
</style>
