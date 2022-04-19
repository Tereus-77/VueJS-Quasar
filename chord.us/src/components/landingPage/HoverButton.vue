<template>
  <div class="row button-outer justify-between">
    <div class="col-9 button-left">{{ buttonText }}</div>
    <!--<div class="button button-solid button-right col-3 text-align-center">
      <img src="/img/btn-arrow.svg" />
    </div>-->
    <BasicButton
      button-text=""
      use-background
      color="#007FA9"
      :on-click="onClick"
    />
  </div>
</template>
<script>
import BasicButton from 'components/landingPage/BasicButton'
export default {
  components: {
    BasicButton
  },
  props: {
    buttonText: { type: String, required: true },
    onClick: { type: Function, required: true }
  },
  data() {
    return {}
  }
}
</script>
<style scoped>
.button-outer {
  border: 0px;
  background-color: #ffffff;
  padding: 2px;
  border-radius: 30px;
  margin-top: 30px;
  cursor: pointer;
}

.button-outer:hover {
  -webkit-box-shadow: -2px 3px 8px #e0b083;
  box-shadow: -2px 3px 8px #e0b083;
}

.button-left {
  font-weight: bold;
  padding-top: 15px;
  text-indent: 20px;
  font-size: 13pt;
}

.button-right {
  height: 50px;
}

.button img {
  margin: unset !important;
}
</style>
