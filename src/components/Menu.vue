<template>
  <div class="ui top fixed menu">
    <div class="ui container">
      <img src="../assets/logo.svg" class="ui small image" alt="biofacts">
      <div class="ui secondary right menu">
        <a class="item">
          Mision
        </a>
        <a class="item">
          Sumate
        </a>
        <a class="item">
          Calculadora
        </a>
    </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Contribute',
    el: '#contribute',
  }
</script>

<style scoped>
  .secondary.menu.menu a.item {
    font-family: 'Montserrat', sans-serif;
    font-size: 18px;
    font-weight: 600;
  }
  .secondary.menu a.item:hover {
  }

  .menu .container {
    padding-top: 8px;
    padding-bottom: 8px;
  }
</style>
