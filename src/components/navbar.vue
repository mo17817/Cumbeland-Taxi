<template>
<head>
  <link rel="preconnect" href="https://fonts.googleapis.com"/>
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
    <link href="https://fonts.googleapis.com/css2?family=Lobster&family=Satisfy&display=swap" rel="stylesheet"/>
  </head>
  <div class= "q-pa-xxs">
  <q-header elavated>
          <div class="text-black text-center" align = "center" id="title">
                Cumberland Taxi Cab 
        <div class="col-3 text-black" align="right">
        <q-toolbar id = "navbar">
        <q-breadcrumbs class = "text-black" active-color="secondary" style="font-size: 30">
          <q-breadcrumbs-el class = "text-black text-weight-light" icon = "home" label = "Available from 9am to 12pm" type = "button"/>
            <q-breadcrumbs-el class = "text-black text-weight-light" icon = "phone" label = "call today"/>
            <q-btn href = "pages/Form.vue" link = "pages/Form.vue" />
            <q-breadcrumbs-el  class = "text-black text-weight-light text-left"  icon = "car" label = "Book a Ride!" />
        </q-breadcrumbs>
      </q-toolbar>
        </div>
    </div>
  </q-header>
    </div>
</template>

<style lang="css" scoped>
#title{
  font-size: xxx-large;
}
@media screen and (max-width: 400px) {
  #title{
    font-size: xx-large;
  }
}



#Dropdown{
  color: yellow;
}
</style>

<script>
  export default {
    name: "Navbar",
    data() {
      return {
       currentPage: "",
       value: ""
      }
    },
    methods: {
    }
  }
</script>

