<template>
  <v-footer dark padless app inset>
    <v-cart
      class="flex"
      flat
      title
      style="background-color: #4d4dff"
      color="blue lighten-1"
      :elevation="10"
    >
      <v-card-text class="py-2 white--text text-center">
        {{ new Date().getFullYear() }} - <strong> techIdea</strong>
      </v-card-text>
    </v-cart>
  </v-footer>
</template>
