<template>
  <div>
    <q-header class="bg-white">
      <q-toolbar>
        <!-- <div class="float-left" style="width:1200px"> -->
        <img
          src="../assets/primary.png"
          srcset="../assets/primary@2x.png 2x, ../assets/primary@3x.png 3x"
          class="primary-logo"
        />
        <q-tabs class="ml-182" align="left">
          <q-route-tab to="/home" label="Search Rates" />
          <q-route-tab to="/about" label="Plan A Shipment" />
          <q-route-tab to="/bookings" label="Bookings" />
          <q-route-tab to="/shipments" label="Shipments" />
          <q-route-tab to="/my-account" label="My Account" />
        </q-tabs>
        <!-- </div> -->
        <div class="float-right" style="color:black; width:235px">
          <div class="float-right">
            <!-- <div class="right-of-header"> -->
            <img
              src="../assets/notification.png"
              srcset="../assets/notification@2x.png 2x, ../assets/notification@3x.png 3x"
              class="notification-icon mr-24"
            />
            <!-- </div>
            <div class="right-of-header">-->
            <img
              src="../assets/group.png"
              srcset="../assets/group@2x.png 2x, ../assets/group@3x.png 3x"
              class="profile-pic"
            />
            <!-- </div> -->
          </div>
        </div>
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
  /* width: 1440px; */
  margin: 0 auto;
  /* background-color: #ffffff;
  box-shadow: 0 0 50px 0 var(--very-light-pink); */
}
.q-tab:first-child {
  width: 190px !important;
  height: 80px !important;
  border-left: solid 1px var(--very-light-pink);
  border-right: solid 1px var(--very-light-pink);
  color: var(--black);
}
.q-tab {
  width: 190px !important;
  padding-right: 32px !important;
  padding-left: 32px !important;
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
.primary-logo {
  width: 49px;
  height: 48px;
  object-fit: contain;
}
.header-backgound {
  height: 80px !important;
  width: 1440px;
  margin: 0 auto;
  /* background-color: #ffffff;
  box-shadow: 0 0 50px 0 var(--very-light-pink); */
}
.q-toolbar {
  width: 1440px !important;
  margin: 0 auto !important;
}
.notification-icon {
  width: 29px;
  height: 29px;
  object-fit: contain;
}
.profile-pic {
  width: 48px;
  height: 48px;
  object-fit: contain;
}
.right-of-header {
  display: inline-block;
}
</style>
