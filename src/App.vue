<template>
  <div>
      {{ count }}
      <h1>{{ rowHtml }}</h1>
      <h2 v-html="rowHtml2"></h2>

      <div :class="{ active : isActive }">Is it green?</div>
      <button @click="change">Button</button>

      <h3>Style Binding</h3>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isVisible : false,
    }
  }
  
}
</script>

<style scoped>
h2.active {
  color: green;
}

</style>