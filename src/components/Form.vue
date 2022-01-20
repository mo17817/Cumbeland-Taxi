<template>
  <div class="q-pa-md text-black bg-primary full-width border">
    <form class="q-gutter-md" @submit.prevent="sendEmail" ref="serviceForm">
      <q-input
        filled
        name="name"
        :color="this.color"
        v-model="name"
        label="Your name *"
        hint="Name and surname"
        lazy-rules
        :rules="[(val) => (val && val.length > 0) || 'Please type something']"
        required
      />
      <q-input
        filled
        name="email"
        v-model="email"
        label="Your Email"
        hint="Enter your email"
        lazy-rules
        :rules="[(val) => (val && val.length > 0) || 'Please type something']"
        required
      />
      <q-input
        name="city"
        label="Your city"
        hint="Name of your city"
        filled
        v-model="city"
        required
      ></q-input>
  
      <q-input
        filled
        class="text-white"
        v-model="datetime"
        type="datetime-local"
        value="2021-12-12T19:30"
        min="2021-12-07T00:00"
        max="2021-14-14T00:00"
        name="datetime"
        hint="Please select the date and time of your appointment"
        required
      />
    <q-input
        filled 
        class = "text-white"
        name = "number"
        hint = "Include area code please"
        label = "Phone Number"
     />

      <div align="center">
        <q-btn label="Submit" type="submit" color="secondary" class = "text-black" />
        <q-btn
          label="Reset"
          type="reset"
          color="primary"
          flat
          class="q-ml-sm"
        />
      </div>
    </form>
  </div>
</template>
<script>
import emailjs from "emailjs-com";
import { ref } from "vue";

export default {
  props: {
    tier: {
      type: String,
      default: "Default prop value",
    },
    color: {
      type: String,
      default: "Primary",
    },
  },
  data() {
    return {
      tierSelected: this.tier,
    };
  },
  setup() {
    // let testing = this.props.tier
    const name = ref(null);
    const city = ref(null);
    const email = ref(null);
    const datetime = ref(null);
    const number = ref(null)

    return {
      name,
      city,
      email,
      datetime,
      number
      // testing,
    };
  },
  methods: {
    sendEmail() {
      emailjs
        .sendForm(
          "service_jzppe1g",
          "template_mu0qgn9",
          this.$refs.serviceForm,
          "user_0kAkG7FRNx8mEzj025Trm"
        )
        .then(
          (res) => {
            console.log(res.text);
            if (res.text == "OK") {
              window.location.href = "#";
            }
          },
          (error) => {
            console.log(error.text);
          }
        );
    },
  },
};
</script>
