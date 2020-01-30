<template>
  <v-card
      elevation="12"
      max-width="800"
      class="mx-auto"
  >
    <v-card-title class="pa-1 align-center justify-center">
      <v-icon class="top-icon" large color="indigo darken-3">mdi-link-variant</v-icon>
      <h2>Accounts</h2>
    </v-card-title>

    <div class="text-center pa-5">
      <v-tooltip bottom>
        <template v-slot:activator="{on}">
          <v-btn
              class="mx-3"
              fab
              dark
              large
              color="blue"
              elevation="7"
              v-on="on"
              href="https://twitter.com/fres_nel"
          >
            <v-icon dark large>mdi-twitter</v-icon>
          </v-btn>
        </template>
        <span>Twitter</span>
      </v-tooltip>

      <v-tooltip bottom>
        <template v-slot:activator="{on}">
          <v-btn
              class="mx-3"
              fab
              dark
              large
              color="blue-grey"
              elevation="7"
              v-on="on"
              href="https://github.com/fres-nel"
          >
            <v-icon dark large>mdi-github-circle</v-icon>
          </v-btn>
        </template>
        <span>Github</span>
      </v-tooltip>

      <v-tooltip bottom>
        <template v-slot:activator="{on}">
          <v-btn
              class="mx-3"
              fab
              dark
              large
              color="teal"
              elevation="7"
              v-on="on"
              href="https://github.com/fres-nel"
          >
            <v-icon dark large>mdi-book-open</v-icon>
          </v-btn>
        </template>
        <span>Blog</span>
      </v-tooltip>

      <v-tooltip bottom>
        <template v-slot:activator="{on}">
          <v-btn
              class="mx-3"
              fab
              dark
              large
              color="orange"
              elevation="7"
              v-on="on"
              href="https://speakerdeck.com/fresnel"
          >
            <v-icon dark large>mdi-comment-multiple-outline</v-icon>
          </v-btn>
        </template>
        <span>SpeekerDeck</span>
      </v-tooltip>
    </div>

  </v-card>
</template>

<script>
  export default {
    name: "Accounts"
  }
</script>

<style scoped>
  .top-icon {
    margin-right: 15px;
  }
</style>