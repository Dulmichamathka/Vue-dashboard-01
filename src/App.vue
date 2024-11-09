<template>
  <v-app>
    <NavbarComponent />
    <v-content class="ma-4">
      <router-view> </router-view>
    </v-content>
  </v-app>
</template>

<script>
import NavbarComponent from "./components/NavbarComponent.vue";

export default {
  name: "App",
  components: {
    NavbarComponent,
  },
};
</script>
