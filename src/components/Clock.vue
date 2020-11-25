<template>
  <div>
      <h5>{{ time }}</h5>
  </div>
</template>

<script>
export default {
    name: 'Clock',
    data: function() {
        return {
            msg: 'My Vue',
            time: new Date()
        }
    },
    created: function() {
        setInterval(() => {
            this.time = new Date()
        }, 1000)
    }
}
</script>

<style>

</style>