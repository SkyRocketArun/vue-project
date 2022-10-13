<template>
  <div class="nav_bar">
    <div>This is Navigation bar </div>
    <router-link to="/">Go to HomePage</router-link>
    <router-link to="/sign-up">Go to Sign up</router-link>
  </div>
  <router-view/>
</template>
<script>

export default {
  name: 'App',
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  box-sizing: border-box;
}
.nav_bar a{
  display: inline-block;
  padding:10px;
}
</style>
