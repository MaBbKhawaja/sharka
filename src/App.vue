<template>
  <q-layout view="lHh Lpr lFf">
    <TopNav />
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import TopNav from "./components/TopNav";
export default {
  name: "LayoutDefault",

  components: {
    TopNav
  },

  data() {
    return {
      leftDrawerOpen: false
    };
  }
};
</script>

<style></style>
