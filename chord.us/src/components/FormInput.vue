<template>
  <div
    class="position-relative input-wrapper"
    :class="useTextArea ? 'input-wrapper-tall' : 'input-wrapper'"
  >
    <textarea
      v-if="useTextArea"
      v-model="inputText"
      class="formatted-text-area fs-14 dark-color"
      :class="
        lightTheme
          ? 'dark-color light-background'
          : 'light-color dark-background'
      "
      :placeholder="placeholder"
    ></textarea>
    <input
      v-else
      v-model="inputText"
      :type="inputType"
      class="formatted-text-input fs-14"
      :class="
        lightTheme
          ? 'dark-color light-background'
          : 'light-color dark-background'
      "
      :placeholder="placeholder"
    />
    <label
      v-if="lightTheme"
      class="fs-10 position-absolute input-label dark-color light-background"
      >{{ label }}</label
    >
    <label
      v-else
      class="fs-10 position-absolute input-label light-color dark-background"
      >{{ label }}</label
    >
  </div>
</template>
<script>
export default {
  props: {
    label: { type: String, required: true },
    placeholder: { type: String, required: false, default: '' },
    useTextArea: { type: Boolean, required: false, default: false },
    isPassword: { type: Boolean, required: false, default: false },
    lightTheme: { type: Boolean, required: false, default: true }
  },
  data() {
    return {
      inputText: ''
    }
  },
  computed: {
    inputType() {
      if (this.isPassword) {
        return 'password'
      }
      return 'text'
    }
  },
  methods: {
    onTextChange() {
      this.$emit('inputTextChanged', this.inputText)
    }
  }
}
</script>
<style scoped>
.formatted-text-input,
.formatted-text-area {
  border-radius: 8px;
  position: absolute;
  bottom: 0;
  padding: 7px 18px;
  left: 0;
  width: 100%;
}

.light-background {
  background-color: #fff;
}

.dark-background {
  background-color: var(--dark-color);
}

input.dark-background {
  border: 1px solid #fff;
}

input.light-background {
  border: 1px solid #000;
}

.formatted-text-input {
  height: 45px;
}

.formatted-text-area {
  height: 100px;
}

.input-label {
  top: 8px;
  left: 15px;
  width: fit-content;
  white-space: nowrap;
  padding: 0 5px;
}

.input-wrapper {
  height: 60px;
}

.input-wrapper-tall {
  height: 115px;
}
</style>
