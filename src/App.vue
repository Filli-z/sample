<template>
  <v-app id="inspire">
    <v-app-bar class="px-3" flat density="compact">
      <v-avatar
        color="grey-darken-1"
        class="hidden-md-and-up"
        size="32"
      ></v-avatar>

      <v-spacer></v-spacer>

      <v-tabs centered color="grey-darken-2">
        <v-tab
          v-for="link in links"
          :key="link.text"
          :text="link.text"
          :to="link.link"
        ></v-tab>
      </v-tabs>
      <v-spacer></v-spacer>

      <v-avatar
        class="hidden-sm-and-down"
        color="grey-darken-1"
        size="32"
      ></v-avatar>
    </v-app-bar>

    <v-main class="bg-grey-lighten-3">
      <router-view />
    </v-main>
  </v-app>
</template>

<script setup>
const links = [
  { text: "Slide 1", link: "/slide1" },
  { text: "Slide 2", link: "/slide2" },
];
</script>

<script>
export default {
  data: () => ({}),
};
</script>
