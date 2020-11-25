<template>
  <div id='app-header'>
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
#app-header {
  display: table;
  width: 30%;
}

#app-header > h1, p {
  display: table-cell;
}

#app-header > p {
  text-align: right;
}
</style>