<template>
  <v-app>
    <v-app-bar app class="blue d-flex item-center">
      <v-row cols="11">
          <v-app-bar-nav-icon class="white--text" @click="drawer = !drawer" />
      </v-row>
      <v-row cols="1" align-self="end">
          <v-switch v-model="$vuetify.theme.dark"></v-switch>
      </v-row>
    </v-app-bar>
    <v-navigation-drawer app v-model="drawer" class="blue lighten-4">
      <nav></nav>
    </v-navigation-drawer>
    <v-main>
      <v-container>
        <router-view></router-view>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
// import image from './assets/logo.svg'

export default {
  name: 'App',
  data () {
    return {
      drawer: false,
    }
  },
};
</script>
