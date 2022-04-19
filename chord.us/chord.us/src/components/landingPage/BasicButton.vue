<template>
  <div @click="onClick" :class="classList">
    {{ buttonText }}
    <div v-if="removeIcon" style="display: inline"></div>
    <img
      v-else-if="rotateIcon"
      :src="icon"
      class="inline-img mobile-hide"
      :class="buttonText.length ? 'left-margin' : ''"
      style="transform: rotate(90deg)"
    />
    <img
      v-else-if="!rotateIcon && buttonText.length"
      :src="icon"
      class="inline-img mobile-hide"
      :class="!useBackground ? 'hollow left-margin' : 'left-margin'"
    />
    <img
      v-else
      :src="icon"
      class="inline-img mobile-hide"
      :class="!useBackground ? 'hollow' : ''"
    />
  </div>
</template>
<script>
export default {
  props: {
    buttonText: { type: String, required: true },
    useBackground: { type: Boolean, required: false, default: false },
    useBorder: { type: Boolean, required: false, default: false },
    fontColorClass: { type: String, required: false, default: 'light-color' },
    gridColClass: { type: String, required: false, default: 'col-5' },
    onClick: { type: Function, required: true },
    icon: { type: String, required: false, default: '/img/btn-arrow.svg' },
    removeIcon: { type: Boolean, required: false, default: false },
    rotateIcon: { type: Boolean, required: false, default: false }
  },
  data() {
    return {
      color: '#0b84ac'
    }
  },
  computed: {
    classList() {
      let retval =
        this.fontColorClass +
        ' ' +
        this.gridColClass +
        ' button text-align-center'

      if (this.useBackground) {
        retval += ' button-solid'
      } else if (this.useBorder) {
        retval += ' button-outline'
      } else {
        retval += ' button-hollow'
      }

      return retval
    }
  },
  mounted() {},
  methods: {
    styling() {
      if (this.useBackground) {
        return 'background-color:' + this.color
      } else if (this.useBorder) {
        return 'border: 2px solid ' + this.color
      } else {
        return 'color:' + this.color
      }
    }
  }
}
</script>
<style scoped>
.inline-img {
  display: inline-block;
  height: 20px;
  vertical-align: sub;
}

.button {
  width: fit-content;
  height: 51px !important;
  padding-top: 13px;
}
</style>
<style>
.inline-img.non-white svg {
  fill: #0a1f44;
  stroke: #0a1f44;
}
</style>
