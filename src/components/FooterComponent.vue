<template>
  <v-footer dark padless app inset>
    <v-cart class="flex" flat title color="#000066" :elevation="10">
      <v-card-text class="py-2 white--text text-center">
        {{ new Date().getFullYear() }} - <strong> techIdea</strong>
      </v-card-text>
    </v-cart>
  </v-footer>
</template>
