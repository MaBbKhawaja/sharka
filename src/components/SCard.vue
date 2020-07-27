<template>
  <div class="float-left card-bg">
    <slot name="title"></slot>
    <div class="card-body">
      <slot name="content"></slot>
    </div>
    <slot name="footer"></slot>
  </div>
</template>

<script>
export default {
  components: {},
  name: "SCard",
  data() {
    return {};
  },
  methods: {}
};
</script>

<style>
.card-body {
  padding-top: 32px;
  padding-bottom: 32px;
  background-color: #ffffff;
  width: 100%;
  height: 180px;
  border: 1px solid #c8c8c8;
}

.card-footer {
  width: 100%;
  border-left: 1px solid #c8c8c8;
  border-right: 1px solid #c8c8c8;
  border-bottom: 1px solid #c8c8c8;
}
.card-bg {
  /* box-shadow: 0 0 50px 0 rgba(0, 0, 0, 0.1); */
  background-color: #ffffff;
}
</style>
