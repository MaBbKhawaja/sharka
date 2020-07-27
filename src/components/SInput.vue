<template >
  <div class="input-container">
    <label class="label-input" v-bind:for="fieldId">{{ labelName }}</label>
    <input
      :id="fieldId"
      :class="cssClass"
      :placeholder="placeholder"
      :value="value"
      v-on:input="updateValue($event.target.value)"
    />
    <i :class="iconName"></i>
  </div>
</template>

<script>
export default {
  name: "SInput",

  props: {
    labelName: {
      type: String,
      required: false
    },
    fieldId: {
      type: String,
      required: false
    },
    cssClass: {
      type: String,
      required: false
    },
    placeholder: {
      type: String,
      default: ""
    },
    value: {
      type: String,
      default: ""
    },
    iconName: {
      type: String
    }
  },
  data() {
    return {
      content: this.value
    };
  },

  methods: {
    updateValue: function(value) {
      this.$emit("input", value);
    }
  },
  watch: {
    value(value) {
      this.onChangeFn(value);
    }
  }
};
</script>

<style scoped lang="scss">
/* .q-field--with-bottom {
  padding-bottom: 0px !important;
  height: 48px !important;
  width: 350px !important;
}
.q-field {
  font-size: 18px;
}
.q-field--dense {
  height: 150px;
}
.q-field__control {
  height: 150px;
}
.q-input {
  height: 150px;
}
.sinput {
  height: 150px;
} */
.input-container {
  border: 1px solid var(--very-light-pink);
  display: -ms-flexbox; /* IE10 */
  display: flex;
  width: 350px;
  height: 48px;
  background-color: var(--white);
  padding-left: 16px;
  padding-right: 16px;
  font-size: 18px;
  i {
    padding-top: 16px;
  }
}
input {
  border: none;
  background-color: var(--white);
  width: 100%;
  outline: none;
}
::placeholder {
  color: var(--black);
  opacity: 1;
}

:-ms-input-placeholder {
  color: var(--black);
}

::-ms-input-placeholder {
  color: var(--black);
}
</style>
