<template>
  <div>
    <div @click="toggle">
      <div v-bind:class="[!show ? 'title' : 'open-title']">
        <slot name="title"></slot>
        <!-- <q-btn
          class="q-mr-md"
          size="sm"
          color="secondary"
          round
          dense
          @click="show = !show"
          :icon="show ? 'remove' : 'add'"
        />-->
        <i :class="!show ? 'fas fa-chevron-down': 'fas fa-chevron-up'"></i>
      </div>
    </div>
    <div v-if="show" class="content">
      <slot name="content"></slot>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  name: "SAccordion",
  data() {
    return {
      show: false
    };
  },
  methods: {
    toggle() {
      this.show = !this.show;
    }
  },
  computed: {}
};
</script>

<style lang="scss">
.title {
  padding: 32px 48px;
  cursor: pointer;
  border: 1px solid var(--very-light-pink);
  // position: absolute;
  width: 635px;
  text-align: end;
}
.content {
  padding-left: 48px;
  padding-right: 48px;
  padding-top: 48px;
  border: 1px solid var(--very-light-pink);
  position: relative;
}
.open-title {
  margin-left: 36px;
  margin-right: 36px;
  cursor: pointer;
  position: absolute;
  margin-top: -10px;
  background-color: #ffffff;
  display: block;
  z-index: 100;
  width: 560px;
  padding-left: 12px;
  padding-right: 12px;
  text-align: end;
}
</style>
