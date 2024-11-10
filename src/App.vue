<template>
  <v-app>
    <NavbarComponent />
    <v-content class="ma-4">
      <router-view> </router-view>
    </v-content>
    <FooterComponent />
  </v-app>
</template>

<script>
import FooterComponent from "./components/FooterComponent.vue";
import NavbarComponent from "./components/NavbarComponent.vue";

export default {
  name: "App",
  components: {
    NavbarComponent,
    FooterComponent,
  },
};
</script>
