<template>
  <v-app class="grey lighten-4">
    <NavBar/>
    <v-main class="mx-4 mb4">
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import NavBar from '@/components/NavBar'
export default {
  name: "App",
  components: { NavBar }
};
</script>
