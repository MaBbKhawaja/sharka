<template>
  <div>
    <div class="tabs">
      <ul>
        <li
          v-for="(tab, index) in tabs"
          :class="{ 'is-active': tab.isActive }"
          :key="tab.name + '_' + index"
          @click="selectTab(tab)"
        >
          <a :href="tab.href">{{ tab.name }}</a>
        </li>
      </ul>
      <div class="tabs-details card-footer-border">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "STabs",

  components: {},

  data() {
    return { tabs: [] };
  },

  created() {
    this.tabs = this.$children;
  },
  methods: {
    selectTab(selectedTab) {
      this.tabs.forEach(tab => {
        tab.isActive = tab.name == selectedTab.name;
      });
    }
  },

  validations: function() {
    return {};
  },

  computed: {}
};
</script>

<style>
.tabs {
  float: left;
  width: 100%;
}
ul {
  float: left;
  padding-inline-start: 0px;
  background-color: var(--white);
  width: 100%;
  margin-block-start: 0px;
  margin-block-end: 0px;
  margin-inline-start: 0px;
  border-left: 1px solid #c8c8c8;
  border-right: 1px solid #c8c8c8;
  /* border-bottom: 1px solid #c8c8c8; */
}
li {
  display: inline-block;
  width: 156.75px;
  padding: 16px;
  font-family: Roboto;
  font-size: 10px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  text-align: center;
  color: var(--black);
  cursor: pointer;
}
.tabs-details {
  float: left;
  display: block;
  width: 100%;
}
.is-active {
  background-color: #ffffff;
  font-weight: bold;
  border-bottom: 4px solid var(--red);
}
.is-active > a {
  font-weight: bold;
}
a {
  text-decoration: none;
  font-family: Roboto;
  font-size: 10px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  text-align: center;
  color: var(--black);
}
</style>
