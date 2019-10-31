<template>
  <div id="hero">
    <Menu />
    <div class="ui container">
      <div>
        <iframe class="iframe-round" src="https://www.youtube.com/embed/yU21Dl17iqw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
      <div class="hero--content">
        <p>¿Cuánto tarda en degradarse el envoltorio de un paquete de fideos? ¿Cuánta agua se utiliza para fabricar una resma de papel? ¿Cuánto impactan los productos que compramos? ¿Y si las botellas de agua, además de incluir la "información nutricional", expresaran la "información ambiental relacionada al producto"?</p>
        <p><b>¡Ya lanzamos la campaña #BioFacts con el objetivo de educar a través del packaging y fomentar el consumo responsable!</b></p>
        <p>Considerando la crisis climática y ecológica que estamos atravesando, esta es una grande oportunidad para unirnos y concientizar masivamente.</p>
      </div>
    </div>
  </div>
</template>

<script>
  import Menu from '../Menu.vue'
  import Video from '../Video.vue'

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
    margin-bottom: 30px;
  }
  .hero--content {
    margin-top: 20px;
  }
  .ui.container {
    margin-top: 80px;
  }
  .iframe-round {
      width: 100%;
      height: 320px;
  }
</style>
