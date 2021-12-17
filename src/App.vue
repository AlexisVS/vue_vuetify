<template>
  <v-app>
    <v-app-bar app class="blue">
      <v-row>
        <v-col align-self="center">
          <v-app-bar-nav-icon class="white--text" @click="drawer = !drawer" />
        </v-col>
        <v-col align-self="center">
          <v-switch></v-switch>
        </v-col>
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
