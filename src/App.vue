<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div>
        <img
          alt="Gap Logo"
          class="mr-2"
          :aspect-ratio="1"
          :src="require('./assets/GapNoName.png')"

          height="64"
        />

        <img
          alt="Grow A Pair"
          class="shrink mt-1 hidden-sm-and-down"
          style="vertical-align:center"
          :src="require('./assets/Gap.png')"
          height="32"
        />
      </div>
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
