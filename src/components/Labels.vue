<template>
  <div id="labels">
    <h1>Etiquetas</h1>
    <div v-for="(product, index) in computedProducts" :key="index">
    <div>{{product.name}}</div>
    <div>{{product.year}}</div>
    <div>{{product.category}}</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Labels',
    el: '#labels',
  }
</script>

<style scoped>

</style>
