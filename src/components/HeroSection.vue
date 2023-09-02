<template>
    <div >
      <q-carousel
        animated
        v-model="slide"
        navigation
        infinite
        :autoplay="autoplay"
        arrows
        transition-prev="slide-right"
        transition-next="slide-left"
        @mouseenter="autoplay = false"
        @mouseleave="autoplay = true"
      >
        <q-carousel-slide class="column flex-center" :name="1" img-src="https://cdn.quasar.dev/img/mountains.jpg" >
        <div class="text-center">
         <div class="text-h4" style="color: #fff;"> Welcome to TechNex Solutions</div>
         <div class="text-h6 q-pa-md" style="color: #fff;">Your Path to Innovation and Excellence</div>
        </div>
        </q-carousel-slide>
        <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg" />
        <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg" />
        <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg" />
      </q-carousel>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue'
  
  export default {
    setup () {
      return {
        slide: ref(1),
        autoplay: ref(true)
      }
    }
  }
  </script>
  