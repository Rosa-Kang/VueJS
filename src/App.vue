<template>
  <div>
     <h1>{{ rawHtml }}</h1>
     <h2 v-html="rawHtml2" :class="{ active : isActive }"></h2>
     <button @click="change" >Change Color</button>

     <p>Style Binding Test</p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      rawHtml: 'This is string',
      rawHtml2: 'This is supposed to be varying</span>',
      isActive: false
    }
  },
  methods: {
      change() {
        this.isActive = !this.isActive;
        console.log('button is clicked')
      }
  }
}
</script>

<style scoped>
h2.active {
  color: aquamarine
}
</style>