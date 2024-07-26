<template>
  <div>
      {{ count }}
      <h1>Vue is Mounted</h1>
  </div>
</template>

<script>
export default {
  data () {
    return {
      count: 0,
    }
  },

  beforeCreate() {
    console.log('LifeCycle is beforeCreated', this.count)
  },
  created() {
    console.log('LifeCycle is created', this.count)
  },

  beforeMount() {
    console.log('Lifecycle is beforeMount', document.querySelector('h1'))
  },
  mounted() {
    console.log('Lifecycle is mounted', document.querySelector('h1'))
  },
  
}
</script>

<style lang="scss" scoped>

</style>