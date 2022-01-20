<template>
<q-carousel id ="carousel"
      animated
      v-model="slide"
      navigation
      infinite
      :autoplay="autoplay"
      arrows
      transition-prev="slide-right"
      transition-next="slide-left"
      @mouseenter="autoplay = true"
      @mouseleave="autoplay = true"
      height="500px"
      dark
      arows
    >
      <q-carousel-slide :name="1" img-src= "~assets/sideview.jpg"/>
      <q-carousel-slide :name="2" img-src="~assets/frontview.jpg"  />
      <q-carousel-slide :name="3" img-src = "~assets/interior1.jpg"/>         
      <q-carousel-slide :name="4" img-src = "~assets/interior2.jpg" />
    </q-carousel>
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
<style>
    #carousel{
        margin-right: 0;
    }

</style>
  