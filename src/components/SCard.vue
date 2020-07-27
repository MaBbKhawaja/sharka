<template>
  <div>
    <slot name="title"></slot>
    <div class="card-body">
      <slot name="content"></slot>
    </div>
    <slot name="footer">
      <!-- <div class="card-footer"></div> -->
    </slot>
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
</style>
