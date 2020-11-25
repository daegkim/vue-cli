<template>
  <div id="app">
    <app-header v-bind:msg='title' v-bind:user='user'/>
    <clock/>
    <app-article v-on:setUser='setUser'/>
  </div>
</template>

<script>
import Clock from './components/Clock.vue'
import AppHeader from './components/AppHeader.vue'
import AppArticle from './components/AppArticle.vue'

export default {
  name: 'App',
  data: function() {
    return {
      title: 'My Vue',
      user: ''
    }
  },
  components: {
    Clock: Clock,
    AppHeader: AppHeader,
    AppArticle: AppArticle
  },
  methods: {
    setUser: function(arg) {
      this.user = arg.user
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  /*margin-top: 60px;*/
}
</style>
