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

<style>
.q-page-container {
  width: 1110px !important;
}
.q-layout {
  width: 1440px !important;
  margin: 0 auto;
}
.q-header {
  width: 100%;
  /* margin: 0 auto; */
  background-color: #ffffff;
  box-shadow: 0 0 50px 0 var(--very-light-pink);
}
</style>
