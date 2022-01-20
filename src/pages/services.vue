<template>
    <div>
        <Carousel />
        <Carousel3 />
    </div>
</template>
<script>
import { ref } from "vue";
import Carousel from "src/components/Carousel.vue";
import Carousel3 from "components/Carousel3.vue";

export default {
  components: { Carousel, Carousel3 },
  setup() {
    return {
      slide: ref(1),
    };
  },
  data() {
    return {
      serviceCards: {
        interiorDetailing: [
          {
            id: "Interior-Car",
            header: "What we offer",
            title: "Interior Car Detailing",
            description:
              "interior car detailing requires more effort and time than exterior detailing. A dirty interior cabin not only has a bad odor, but also adds to operational complications.Dirty air exhaust spreads allergens about the cabin; stain and grit causes switches to fail; and hazy windows can obscure the view of a driver. In that case, cleaning a car’s interior is more than just washing with water and soap.",
            price: "350 dollars",
            class: "my-card bg-black",
            // imgsrc1: [require("../assets/before1.jpeg")],
            // imgsrc2: [require("../assets/after1.jpeg")],
          },
        ],
        exteriorDetailing: [
          {
            id: "Exterior-Car",
            title: "Exterior Car Detailing",
            description:
              "Exterior car detailing is not just a quick wash of the exterior components of a car. A good car detailer will make the car gleam, minimize surface scratches, and should always apply a shielding paint sealant",
            class: "my-card bg-black",
            // imgsrc1: [require("../assets/before4.jpeg")],
            // imgsrc2: [require("../assets/after17.jpeg")],
          },
        ],
      },
    };
  },

  methods: {
    prev() {
      this.slide.value--;
    },
  },
};
</script>
