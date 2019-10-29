<template>
  <div id="join-the-move">
    <div class="ui container grid">
      <div class="row">
        <div class="right floated eight wide column">
          <h1>SUMATE</h1>
        </div>
      </div>
      <div class="row">
        <div class="eight wide column">
          <vueper-slides class="no-shadow" :visible-slides="3" :autoplay="true" :arrows="false" :pauseOnHover="false" :bullets="false">
            <vueper-slide
              v-for="(slide, i) in slides"
              :key="i"
              :image="slide.image"
            ></vueper-slide>
          </vueper-slides>
        </div>
        <div class="eight wide column">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import { VueperSlides, VueperSlide } from 'vueperslides';

  export default {
    components: { VueperSlides, VueperSlide },
    data: () => ({
      slides: [
        {
          image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSTnSIOhuNr0lB5xDPTPyWluGZmSCxTVM9B5vfgDTA3E7PoRbOg',
        },
        {
          image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTc8bfjZk0HNaNx8zQxDdf2Ey6hXCwNM5L7BEEnturw6_Dm_bNq',
        },
        {
          image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSTnSIOhuNr0lB5xDPTPyWluGZmSCxTVM9B5vfgDTA3E7PoRbOg',
        },
        {
          image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTc8bfjZk0HNaNx8zQxDdf2Ey6hXCwNM5L7BEEnturw6_Dm_bNq',
        },
      ]
    }),
    name: 'JoinTheMove',
    el: '#join-the-move',
  }
</script>

<style scoped>
  .ui.container.grid {
    margin-top: 80px;
  }
</style>
