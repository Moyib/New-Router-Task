<template>
  <div id="app">
    <h1>ROUTER TASK OHHH!!!</h1>
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/contact">Contact</router-link>
    </nav>
    <router-view></router-view>
  </div>
</template>

<script>
import Vue from 'vue'
import VueRouter from 'vue-router'


Vue.use(VueRouter)

const Home = {
  template: '<div>Home</div>'
}
const About = {
  template: '<div>About</div>'
}
const Contact = {
  template: '<div>Contact</div>'
}
const router = new VueRouter({
  routes: [
    { path: '/', component: Home },
    { path: '/about', component: About },
    { path: '/contact', component: Contact },
  ]
});

new Vue({
  router
}).$mount('#app')

export default {
  name: 'App'
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
