<template>
  <div id="hero">
    <Menu />
    <div class="ui container grid">
      <div class="eight wide column">
        <Video />
      </div>
      <div class="eight wide column">
        <h1>Mision</h1>
        <p>Buscamos concientizar sobre la importancia de nuestro impacto en la tierra, creemos que es necesario que el ser humano se solidarice, se sienta parte del ambiente que lo rodea.</p>
      </div>
    </div>
  </div>
</template>

<script>
  import Menu from './Menu.vue'
  import Video from './Video.vue'

  export default {
    name: 'Hero',
    el: '#hero',

    components: {
      Menu,
      Video
    }
  }
</script>

<style scoped>
  #hero {
    height: 100%;
    min-height: 400px;
  }
  .ui.container.grid {
    margin-top: 60px;
  }

</style>
