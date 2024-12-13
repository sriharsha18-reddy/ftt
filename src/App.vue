<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <ul class="navbar-links">
    <li><router-link to="/" :class="{'dark-theme': isDarkMode, 'light-theme': !isDarkMode}">Home</router-link></li>
    <li v-if="!isLoggedIn"><router-link to="/signup" :class="{'dark-theme': isDarkMode, 'light-theme': !isDarkMode}">Signup</router-link></li>
    <li v-if="!isLoggedIn"><router-link to="/login" :class="{'dark-theme': isDarkMode, 'light-theme': !isDarkMode}">Login</router-link></li>
    <li v-if="isLoggedIn"><router-link to="/profile" :class="{'dark-theme': isDarkMode, 'light-theme': !isDarkMode}">Profile</router-link></li>
    <li v-if="isLoggedIn"><router-link to="/dashboard" :class="{'dark-theme': isDarkMode, 'light-theme': !isDarkMode}">Dashboard</router-link></li>
  </ul>
<router-view></router-view>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
