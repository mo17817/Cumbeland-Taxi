<template>
  <head>
     <link rel="preconnect" href="https://fonts.googleapis.com"/>
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
    <link href="https://fonts.googleapis.com/css2?family=Lobster&family=Satisfy&display=swap" rel="stylesheet"/>
    <link rel="preconnect" href="https://fonts.googleapis.com"/>
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
    <link href="https://fonts.googleapis.com/css2?family=Exo+2:wght@300&display=swap" rel="stylesheet"/>
  </head>
  <q-separator color="secondary" size="4px" />
  <div class="q-pa-sm bg-primary" id ="first-container">
    <Parallax></Parallax>
    <!-- first horizontal card -->
  <div class="q-pb-lg row items-start bg-primary text-black">
    <q-card class="my-card bg-primary" flat bordered id = "second-para">
      <q-card-section horizontal bordered>
        <q-card-section>
          <div class = "col" align = "left">
            <h2> Give us a Call Today ! </h2>
             <q-separator class = "bg-secondary" color="primary" size="6px" />
              <h4> We offer the best and most reliable rides and bookings in all of Portland. Snow, skeet or rain Cumberland Taxi is the ride for you come experience the Cumberland Taxi way of transportation! Call <u>207-808-9792</u> </h4>
            </div>
        </q-card-section>
        <q-img
          src="~assets/winter-pic.jpeg"
          height = "497px"
          id = "img"
        />
      <q-separator color="secondary" size="8px" />
      </q-card-section>
    </q-card>
  </div>
<!-- end -->
    <div id="carousel-container">
      <div class="col" id="text-container"></div>

      <q-separator color="secondary" size="8px" />

      <carousel></carousel>
    </div>
    <q-separator color="secondary" size="8px" />
    <!-- first card -->
    <div class="row q-ma-sm bg-primary">
      <div class="row q-ma-sm" id="first-card">
        <!--first q-card-->
        <q-card
          v-for="object in infoCards"
          :key="object"
          :class="object.class"
          :id="object.id"
        >
          <q-card-section horizontal>
            <q-card-section>
              <div class="col">
                <h2 class="text-black" align="center" id="first-para">
                  {{ object.title }}
                </h2>
                <div align="center" id = "btn-container">>
                  <q-btn align="center"
                  rounded
                  shadow
                  @click="object.Form"
                  id = "a-btn">
                    <h6
                      class="text-black text-weight-bold"
                      id="first-para"
                      align="center"
                    >
                      {{ object.hours }}

                    </h6>
                  </q-btn>
                  <div
                  align = "center"
                  class = "q-pa-md text-black"
                  >
                  <q-btn
                    to = "src/pages/form"
                    rounded
                    shadow
                    class = "q-pa-md"
                    id = "a-btn"
                    >
                    <h6 id="first-para" class="text-black text-weight-bold">
                      <u> click here to book an appointment today !</u> </h6>
                  </q-btn>
                  </div>
                </div>
                <q-dialog>
                  <q-btn rounded>
                  </q-btn>
                </q-dialog>
                <div class="col q-ma-sm" align="center">
                  <q-avatar rounded size="70px">
                    <q-img align="center" src="~assets/taxi-logo.jpg" />
                  </q-avatar>
                </div>

                <q-separator horizontal color="bg-secondary" />
                <div align="center">
                  <h6 class="text-black text-weight-light" id="first-para">
                    <h3>{{ object.title1 }}</h3>
                    <lb />
                    <u>
                      {{ object.description }}
                    </u>
                  </h6>
                </div>
              </div>
            </q-card-section>
          </q-card-section>
        </q-card>
        <Form> </Form>
      </div>
      <!--page scroller-->
      <q-page-scroller
        position="bottom-right"
        :scroll-offset="200"
        :offset="[18, 18]"
      >
        <q-btn icon="keyboard_arrow_up" color="secondary" />
      </q-page-scroller>
    </div>
    <!-- <div class="col" align="center">
      <h1 class="text-white" id="review-header">
        Hear from our loyal patrons!
      </h1>
      <Carousel3> </Carousel3>
    </div> -->
  </div>
</template>
<script>
import { ref } from "vue";
import Carousel from "src/components/Carousel.vue";
import Carousel3 from "components/Carousel3.vue";
import Form from "components/Form.vue";
import Parallax from 'components/Parallax.vue';

export default {
  components: { Carousel, Form, Parallax, },
  setup() {
    return {
      slide: ref(1),
    };
  },
  data() {
    return {
      infoCards: [
        {
          id: "mission-statement",
          title:
            "Welcome to Cumberland Taxi Cab where we offer the best and fastest servcies avaliable!",
          description:
            "At Cumberland County taxi we service Portland maine, Oldport,Downtown , Jetport Airport, Cumberland, Westbrook, Scarborough, Cape Elizabeth, Maine Mall, USM, South Portland, Old Orchard Beach, Falmouth, plus more!",
          class: "my-card bg-primary text-white",
          title1: "Cumberland Taxi, Your most reliable transportation services",
          hours: "Our hours are from 10:00am - 11:00pm Mon-Sun !",
          Form: "<Form/>",
        },
      ],
    };
  },
};
</script>
<style>
#call{
  font-family: 'Exo 2', sans-serif;
  font-size: 55px;
}
#title {
  font-family: "Lobster";
  font-size: 50px;
  /* font-weight: bold; */
  /* position:sticky; */
}
#breath-mint {
  font-family: "Lobster";
  font-size: 35px;
  /* position: fixed; */
  /* font-weight: initial; */
}
#first-para {
  font-family: 'Exo 2', sans-serif;
}
#second-para {
  font-family: 'Exo 2', sans-serif;
  font-size: 15px;
  display: wrap;
  flex-wrap: wrap;
}
#second-card {
  margin: 7px;
  display: wrap;
  flex-wrap: wrap;
}
#header {
  position: relative;
  padding-top: 0%;
  padding-bottom: 0%;
  margin-top: 0%;
  margin-bottom: 0%;
}
#First-Object {
  size: 45px;
  color: "yellow";
}
#btn-container{
  display: flex;
  justify-content: space-evenly;
  font-family: 'Exo 2', sans-serif;
}
#a-btn:hover{
    color: #a9e8e2;
    background: #a9e8e2;
}

@media screen and (max-width: 400px) {
  #review-header {
    font-size: x-large;
    direction: flex;
  };
  #second-para{
    font-size: x-small;
    direction: flex;
  }
  #first-container{
    font-size: x-small;
    width: auto;
    margin: auto;
    direction: flex;
  }
  #first-para{
    font-size: small;
    margin: auto;
    width: auto;
    direction: flex;
  }
  #img{
    display: wrap;
    flex-wrap: wrap;
    size: small;
    justify-content: space-evenly;
  }
  #btn-container{
    size: xx-small;
    font-size: xx-small;
  }
}
</style>
