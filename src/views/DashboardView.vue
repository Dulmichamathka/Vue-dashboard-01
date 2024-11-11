<template>
  <div>
    <h2 class="subheading grey--text mb-2">Dashboard</h2>
    <v-container class="ms-0">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3>
          <v-card class="ma-3" style="height: 118px">
            <v-list-item>
              <v-list-item-avatar
                tile
                class="mt-n7 customradius"
                style="
                  height: 75px;
                  min-width: 75px;
                  width: 40px;
                  border-radius: 5px !important;
                "
              >
                <v-sheet
                  color="green"
                  width="72"
                  height="65"
                  style="border-radius: 8px"
                  elevation="10"
                >
                  <v-icon dark large>home</v-icon>
                </v-sheet>
              </v-list-item-avatar>
              <v-list-item-content class="pb-0">
                <div class="overline text-right">Article</div>
                <v-list-item-title class="headline mb-1 text-right"
                  >523661</v-list-item-title
                >
                <div><v-divider></v-divider></div>
              </v-list-item-content>
            </v-list-item>
            <v-card-actions class="pt-0">
              <v-icon text class="ma-2">person</v-icon>
              <div class="overline">Dulmi</div>
            </v-card-actions>
          </v-card>
        </v-flex>

        <v-flex xs12 sm6 md4 lg3>
          <v-card class="ma-3" style="height: 118px">
            <v-list-item>
              <v-list-item-avatar
                tile
                class="mt-n7 customradius"
                style="
                  height: 75px;
                  min-width: 75px;
                  width: 40px;
                  border-radius: 5px !important;
                "
              >
                <v-sheet
                  color="green"
                  width="72"
                  height="65"
                  style="border-radius: 8px"
                  elevation="10"
                >
                  <v-icon dark large>home</v-icon>
                </v-sheet>
              </v-list-item-avatar>
              <v-list-item-content class="pb-0">
                <div class="overline text-right">Article</div>
                <v-list-item-title class="headline mb-1 text-right"
                  >523661</v-list-item-title
                >
                <div><v-divider></v-divider></div>
              </v-list-item-content>
            </v-list-item>
            <v-card-actions class="pt-0">
              <v-icon text class="ma-2">person</v-icon>
              <div class="overline">Dulmi</div>
            </v-card-actions>
          </v-card>
        </v-flex>

        <v-flex xs12 sm6 md4 lg3>
          <v-card class="ma-3" style="height: 118px">
            <v-list-item>
              <v-list-item-avatar
                tile
                class="mt-n7 customradius"
                style="
                  height: 75px;
                  min-width: 75px;
                  width: 40px;
                  border-radius: 5px !important;
                "
              >
                <v-sheet
                  color="green"
                  width="72"
                  height="65"
                  style="border-radius: 8px"
                  elevation="10"
                >
                  <v-icon dark large>home</v-icon>
                </v-sheet>
              </v-list-item-avatar>
              <v-list-item-content class="pb-0">
                <div class="overline text-right">Article</div>
                <v-list-item-title class="headline mb-1 text-right"
                  >523661</v-list-item-title
                >
                <div><v-divider></v-divider></div>
              </v-list-item-content>
            </v-list-item>
            <v-card-actions class="pt-0">
              <v-icon text class="ma-2">person</v-icon>
              <div class="overline">Dulmi</div>
            </v-card-actions>
          </v-card>
        </v-flex>

        <v-flex xs12 sm6 md4 lg3>
          <v-card class="ma-3" style="height: 118px">
            <v-list-item>
              <v-list-item-avatar
                tile
                class="mt-n7 customradius"
                style="
                  height: 75px;
                  min-width: 75px;
                  width: 40px;
                  border-radius: 5px !important;
                "
              >
                <v-sheet
                  color="green"
                  width="72"
                  height="65"
                  style="border-radius: 8px"
                  elevation="10"
                >
                  <v-icon dark large>mdi-home</v-icon>
                </v-sheet>
              </v-list-item-avatar>
              <v-list-item-content class="pb-0">
                <div class="overline text-right">Article</div>
                <v-list-item-title class="headline mb-1 text-right"
                  >523661</v-list-item-title
                >
                <div><v-divider></v-divider></div>
              </v-list-item-content>
            </v-list-item>
            <v-card-actions class="pt-0">
              <v-icon text class="ma-2">person</v-icon>
              <div class="overline">Dulmi</div>
            </v-card-actions>
          </v-card>
        </v-flex>
        <!-- Display team members dynamically -->
        <v-flex xs12 sm6 lg3 v-for="person in team" :key="person.name">
          <v-card class="text-center ma-3">
            <v-responsive class="pt-4">
              <v-avatar size="100" class="blue lighten-2">
                <v-img :src="person.avatar"></v-img>
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{ person.name }}</div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn outlined color="orange">
                <v-icon small left>mdi-message</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      team: [
        { name: "Dulmi", role: "Front-End developer", avatar: "/img5.jpeg" },
        { name: "Geeth", role: "Fullstack developer", avatar: "/img4.jpeg" },
        { name: "Niluka", role: "Web designer", avatar: "/img3.jpeg" },
        { name: "Manoj", role: "Web developer", avatar: "/img1.jpg" },
      ],
    };
  },
};
</script>

<style>
.customradius {
  border-radius: 5px;
}
</style>
