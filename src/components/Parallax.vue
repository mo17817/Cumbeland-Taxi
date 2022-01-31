<template>
<head>
    <link rel="preconnect" href="https://fonts.googleapis.com"/> 
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/> 
    <link href="https://fonts.googleapis.com/css2?family=Exo+2:wght@300&display=swap" rel="stylesheet"/>
</head>
  <div class="q-pa-md" id = "parallax">
    <q-parallax :height="350" :speed="0.5">
      <template v-slot:media>
        <img src="~assets/portland_streets3.jpeg" size = "250px">
      </template>

      <h1 class="bg-transparent text-primary"><i>Cumberland Taxi</i></h1>
    </q-parallax>
  </div>
</template>
<style scoped>
#parallax{
    font-family: 'Exo 2', sans-serif;
}
</style>