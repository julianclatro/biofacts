<template>
  <div id="upcomming">
    <div class="ui grid container">
      <div class="column">
        <h1>Próximamente</h1>
        <p>¡Productos y empresas que ya se sumaron!</p>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'Upcomming',
    el: '#upcomming',
  }
</script>

<style scoped>
  #upcomming {
    margin-top: 40px;
    background: #09433B;
    padding-top: 40px;
    padding-bottom: 40px;
  }
  .ui.grid.container {
    color: white;
  }
</style>
