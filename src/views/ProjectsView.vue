<template>
  <div class="project">
    <h1 class="subheading grey--text">Projects</h1>
    <v-container>
      <v-layout row wrap class="mb-7">
        <v-tooltip bottom>
          <template v-slot:activator="{ on }">
            <v-btn
              small
              outlined
              color="green"
              @click="sortBy('title')"
              class="mr-2"
              dark
              v-on="on"
            >
              <v-icon left small> folder</v-icon>
              <span class="caption text-lowercase">By project title</span>
            </v-btn>
          </template>
          <span>sort project</span>
        </v-tooltip>
        <v-tooltip bottom>
          <template v-slot:activator="{ on }">
            <v-btn
              small
              outlined
              color="green"
              @click="sortBy('title')"
              class="mr-2"
              dark
              v-on="on"
            >
              <v-icon left small>person</v-icon>
              <span class="caption text-lowercase">By name</span>
            </v-btn>
          </template>
          <span>sort person</span>
        </v-tooltip>
      </v-layout>

      <v-card v-for="project in projects" :key="project.title" class="mb-1">
        <v-layout row wrap :class="`pa-3 project  ${project.status}`">
          <v-flex cs12 md6>
            <div class="caption gray--text">Person</div>
            <div>{{ project.person }}</div>
          </v-flex>
          <v-flex xs-6 sm4 md2>
            <div class="caption gray--text">Out By</div>
            <div>{{ project.due }}</div>
          </v-flex>
        </v-layout>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    projects: [
      {
        title: "Site web",
        person: "dulmi",
        due: "10/10/1987",
        status: "complete",
      },
      {
        title: "Application mobile",
        person: "Geeth",
        due: "02/10/1987",
        status: "no",
      },
      {
        title: "Hotel management site",
        person: "Rayan",
        due: "05/05/1987",
        status: "complete",
      },
      {
        title: "conception",
        person: "dulmi",
        due: "10/08/1987",
        status: "yes",
      },
    ],
  }),

  methods: {
    sortBy(prop) {
      this.projects.sort((a, b) => (a[prop] < b[prop] ? -1 : 1));
    },
  },
};
</script>

<style>
.project.complete {
  border-left: 4px solid #3cd1c2;
}

.project.no {
  border-left: 4px solid #ffa600;
}

.project.up {
  border-left: 4px solid #e5464e;
}

.project.yes {
  border-left: 4px solid #c7e80f;
}
</style>
