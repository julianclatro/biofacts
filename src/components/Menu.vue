<template>
  <div class="ui top fixed menu">
    <div class="ui container">
      <img src="../assets/logo.svg" class="ui small image" alt="biofacts">
      <div class="ui secondary right menu">
        <a class="item" href="#hero">
          Mision
        </a>
        <a class="item" href="#join-the-move">
          Sumate
        </a>
        <a class="item" href="#biofacts">
          Calculadora
        </a>
      </div>
    </div>
    <div class="item">
      <a class="">
        <i class="instagram icon"></i>
      </a>
      <a class="">
        <i class="facebook icon"></i>
      </a>
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
