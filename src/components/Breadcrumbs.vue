<template>
  <div class="shark-breadcrumb">
    <span class="shark-breadcrumb-text">Bookings - Booking Name - </span>
    <span style="font-weight: bold;color: var(--black);">Confirm Booking</span>
  </div>
</template>

<script>
export default {
  name: "Breadcrumbs",

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
.shark-breadcrumb {
  font-family: Roboto;
  font-size: 18px;
}
.shark-breadcrumb-text {
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  font-weight: normal;
  color: var(--brown-grey);
}
</style>