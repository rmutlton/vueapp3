<template>
  <v-app>
    <v-navigation-drawer app>
      <p>navigation drawer</p>
    </v-navigation-drawer>

    <v-app-bar app>
      <p>app bar</p>
    </v-app-bar>

    <v-main>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer app>
      <p>footer</p>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      message: "RMUTL",
    };
  },
};
</script>

<style>
</style>