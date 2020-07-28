<template>
  <div @click="onClick" class="button">{{label}}</div>
</template>

<script>
export default {
  name: "SButton",

  props: {
    onClick: {
      type: Function,
      required: true
    },
    label: {
      type: String,
      required: true
    }
  },
  data() {
    return {};
  },

  methods: {}
};
</script>

<style>
.button {
  font-family: Roboto;
  font-size: 16px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  text-align: center;
  color: #ffffff;
  border-radius: 1px;
  background-color: #d8d8d8;
  width: 100%;
  padding: 16px;
  border: 1px solid;
  cursor: pointer;
}
</style>
