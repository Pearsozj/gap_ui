<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-inline-flex">
        <v-img
          alt="Gap Logo"
          class="mr-2"
          contain
          :src="require('./assets/GapNoName.png')"
          transition="scale-transition"
          height="64"
          width="64"
        />

        <v-img
          alt="Grow A Pair"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          :src="require('./assets/Gap.png')"
          width="100"
          height="50"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        target="_blank"
        text
      >
        <span class="mr-2">Add a new account</span>
        <v-icon>mdi-account-circle</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  })
}
</script>
