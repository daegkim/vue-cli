<template>
  <div>
    <ul>
      <li v-for='(v, k) in list' v-bind:key='k' v-on:click='setUser(k)'>{{ v }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'AppArticle',
  data: function() {
    return {
      list: ['john', 'mike', 'kate']
    }
  },
  methods: {
    setUser: function(k) {
      this.$emit('setUser', {
        user: this.list[k]
      })
    }
  }
}
</script>

<style>
  ul {
    padding-left: 20px;
  }

  ul > li {
    list-style: circle;
  }
</style>