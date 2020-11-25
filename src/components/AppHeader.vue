<template>
  <div>
    <h1>{{ msg }}</h1>
    <p>{{ welcomeMsg }}</p>
  </div>
</template>

<script>
export default {
  name: 'AppHeader',
  props: ['msg', 'user'],
  computed: {
    welcomeMsg: function() {
      let result = (this.user === '') ? '' : 'welcome ' + this.user
      return result
    }
  }
}
</script>

<style>

</style>