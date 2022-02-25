<template>
<head>
  <link rel="preconnect" href="https://fonts.googleapis.com"/>
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
    <link href="https://fonts.googleapis.com/css2?family=Lobster&family=Satisfy&display=swap" rel="stylesheet"/>
    <link rel="preconnect" href="https://fonts.googleapis.com"/>
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
    <link href="https://fonts.googleapis.com/css2?family=Exo+2:wght@300&display=swap" rel="stylesheet"/>
  </head>
  <div class= "q-pa-xxs">
  <q-header elavated>
          <div class="text-black text-center" align = "center" id="title">
               <u id ="cumberland"> Cumberland Taxi Cab </u>
                <lb />
        <div class="col-5 text-black" align="center">

        <q-seperator color = "primary" size = "5px"/>
        <q-toolbar id = "navbar">
        <q-breadcrumbs class = "text-black" active-color="secondary" style="font-size: 30px" id = "title" align = "center">
          <q-breadcrumbs-el class = "text-black text-weight-light"  label = "Available from 9am to 12pm"/>
            <q-breadcrumbs-el class = "text-black text-weight-light" icon = "phone" label = "call today"/>
            <q-breadcrumbs-el  class = "text-black text-weight-light text-left"  icon = "local_taxi" label = "Book a Ride!"  to = "src/pages/form" />
        </q-breadcrumbs>
      </q-toolbar>
        </div>
    </div>
  </q-header>
</div>
<!-- <q-separator class = "bg-secondary" color="black" size="8px" /> -->
</template>
<script>
export default defineComponent({
  setup() {
  },
})
</script>

<style lang="css" scoped>
#title{
  font-size: xxx-large;
  font-family: 'Exo 2', sans-serif;
}
#navbar{
  display: inline-block;
  padding: 0%;
  margin: 0%;
}
@media screen and (max-width: 400px) {
  #title{
    font-size: xx-large;
    direction: flex;
    flex-grow: 100%;
    align-items: center;
    display: inline-block;
    justify-content: space-evenly;
  }
}



#Dropdown{
  color: yellow;
}
</style>

