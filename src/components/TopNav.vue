<template>
  <div>
    <q-header class="bg-white">
      <q-toolbar>
        <q-tabs align="left">
          <q-route-tab to="/home" label="Search Rates" />
          <q-route-tab to="/about" label="Plan A Shipment" />
          <q-route-tab to="/bookings" label="Bookings" />
          <q-route-tab to="/shipments" label="Shipments" />
          <q-route-tab to="/my-account" label="My Account" />
        </q-tabs>
      </q-toolbar>
    </q-header>
  </div>
</template>

<script>
export default {
  name: "TopNav",

  components: {},

  data() {
    return {};
  },

  methods: {},

  created() {},

  validations: function() {
    return {};
  },

  computed: {}
};
</script>

<style>
.q-header {
  height: 80px !important;
  background-color: #ffffff;
  box-shadow: 0 0 50px 0 var(--very-light-pink);
}
.q-tab:first-child {
  width: 190px !important;
  height: 80px !important;
  border-left: solid 1px var(--very-light-pink);
  border-right: solid 1px var(--very-light-pink);
  color: var(--black);
}
.q-tab {
  /* width: 190px !important; */
  padding-right: 32px;
  padding-left: 32px;
  height: 80px !important;
  border-right: solid 1px var(--very-light-pink);
  color: var(--black);
}
.q-tab__label {
  color: var(--black);
}
.q-tab__indicator {
  color: var(--red);
}
.q-tab--active .q-tab__indicator {
  height: 7px;
}
</style>
