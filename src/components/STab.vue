<template>
  <div class="float-left" v-show="isActive">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "STab",

  props: {
    name: { required: true },
    selected: { default: false }
  },

  data() {
    return {
      isActive: false
    };
  },

  computed: {
    href() {
      return "#" + this.name.toLowerCase().replace(/ /g, "-");
    }
  },

  mounted() {
    this.isActive = this.selected;
  },

  validations: function() {
    return {};
  }
};
</script>

<style scoped>
</style>
