<template>
  <q-layout view="lHh Lpr lFf">
    <navbar></navbar>
    <q-page-container>
      <q-page>
        <router-view />
      </q-page>
    </q-page-container>
    <!-- <q-footer>
      <q-toolbar class="bg-black">
        <q-toolbar-title
          class="text-center text-italic text-subtitle2 text-weight-heavy"
        >
          Designed and developed by Mo. For help building your site, email
          mo.codes207@gmail.com
        </q-toolbar-title>
      </q-toolbar>
    </q-footer> -->
  </q-layout>
</template>
<script>
import { defineComponent, ref } from "vue";
import navbar from "../components/navbar.vue";

export default defineComponent({
  name: "MainLayout",

  components: {
    navbar,
  },
});
</script>

<style lang="scss" scoped>
#nav {
  color: black;
}
</style>
