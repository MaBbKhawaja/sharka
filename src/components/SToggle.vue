<template>
  <q-btn-toggle :toggle-color="color" :options="options" v-bind:value="value" @input="handleInput" />
</template>

<script>
export default {
  name: "SToggle",

  props: {
    options: {
      type: Array,
      required: true
    },
    color: {
      type: String,
      required: false
    },
    value: {}
  },

  data() {
    return {
      content: this.value,
      model: []
    };
  },

  methods: {
    handleInput: function(value) {
      console.log(value);
      this.$emit("input", value);
    }
  }
};
</script>

<style>
.q-btn-group {
  border: 1px solid var(--very-light-pink);
  box-shadow: none;
  background-color: #fff;
  border-radius: 0px !important;
  height: 48px;
}
.q-btn {
  font-family: Roboto;
  font-size: 16px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  text-align: center;
  color: var(--black);
  padding-left: 4px;
  padding-right: 4px;
}
</style>
