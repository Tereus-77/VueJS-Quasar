<template>
  <div class="full-width" style="padding: 3vw 0vw 0vw 0vw">
    <div class="row mobile-hide" style="padding-right: 3vw">
      <div class="col-3">
        <img
          src="/img/ce-logo.png"
          class="non-mobile"
          style="width: 50%; float: right; margin-right: 25%"
        />
      </div>
      <div class="col-2">
        <div class="link-container main">
          <a>Products</a>
        </div>
        <div class="link-container">
          <a class="new">ChordVideo</a>
        </div>
        <div class="link-container">
          <a>ChordConnect</a>
        </div>
        <div class="link-container">
          <a>Personalization</a>
        </div>
        <div class="link-container">
          <a>AnswerDash</a>
        </div>
      </div>
      <div class="col-2">
        <div class="link-container main">
          <a>Customers</a>
        </div>
        <div class="link-container main">
          <a>Pricing</a>
        </div>
      </div>
      <div class="col-2">
        <div class="link-container main">
          <a>Company</a>
        </div>
        <div class="link-container">
          <a>Our Story</a>
        </div>
        <div class="link-container">
          <a class="hiring">Join the Team</a>
        </div>
        <div class="link-container">
          <a>Block</a>
        </div>
      </div>
      <div class="col-3" style="padding-left: 4%">
        <div class="row" style="border: 0px; padding: 2px">
          <div
            class="col-9"
            style="
              font-weight: bold;
              padding-top: 15px;
              text-indent: 20px;
              font-size: 13pt;
            "
          >
            Press
          </div>
          <div class="col-3 text-align-center" style="height: 55px">
            <img src="/img/btn-arrow.svg" />
          </div>
        </div>
        <div class="row justify-center">
          <div style="border: 1px solid #eec69e; width: 90%" />
        </div>
        <div class="row" style="border: 0px; padding: 2px; margin-top: 20px">
          <div
            class="col-9"
            style="
              font-weight: bold;
              padding-top: 15px;
              text-indent: 20px;
              font-size: 13pt;
            "
          >
            Investor Relations
          </div>
          <div class="col-3 text-align-center" style="height: 55px">
            <img src="/img/btn-arrow.svg" />
          </div>
        </div>
        <div class="row justify-center">
          <div style="border: 1px solid #eec69e; width: 90%" />
        </div>
        <HoverButton
          button-text="Get in Touch"
          :on-click="getInTouchButtonClicked"
        />
        <!--<div
          class="row"
          style="
            border: 0px;
            background-color: #ffffff;
            box-shadow: -2px 3px 8px #e0b083;
            padding: 2px;
            border-radius: 30px;
            margin-top: 30px;
          "
        >
          <div
            class="col-9"
            style="
              font-weight: bold;
              padding-top: 15px;
              text-indent: 20px;
              font-size: 13pt;
            "
          >
            Get in Touch
          </div>
          <div
            class="button button-solid col-3 text-align-center"
            style="height: 55px"
          >
            <img src="/img/btn-arrow.svg" />
          </div>
        </div>-->
      </div>
    </div>
    <div
      class="mobile-hide"
      style="
        margin: 3.5vw 0vw 1vw 1vw;
        background-color: #f8f0e4;
        border-radius: 25px;
        font-size: 14pt;
        color: #0a1f44;
      "
    >
      <div class="row">
        <div
          class="col-6"
          style="padding: 25px; line-height: 35px; text-indent: 2.5vw"
        >
          &#169; CoudEngage Inc. 2020 and Beyond
        </div>
        <div
          class="col-3"
          style="padding: 25px; line-height: 35px; text-indent: 4vw"
        >
          Terms & Conditions
        </div>
        <div
          class="col-3"
          style="padding: 25px; line-height: 35px; text-indent: 5vw"
        >
          Privacy Policy
        </div>
      </div>
    </div>
    <div class="row desktop-hide" style="padding: 0 3vw">
      <div class="col-5">
        <img
          src="/img/ce-logo.png"
          class="mobile-logo"
          style="margin-bottom: 20px"
        />
      </div>
      <div class="col-7"></div>
      <div class="col-12">
        <div class="link-container main-mobile">
          <a>Products</a>
        </div>
        <div class="link-container">
          <a class="new">ChordVideo</a>
        </div>
        <div class="link-container">
          <a>ChordConnect</a>
        </div>
        <div class="link-container">
          <a>Personalization</a>
        </div>
        <div class="link-container">
          <a>AnswerDash</a>
        </div>
        <div class="link-container main-mobile">
          <a>Customers</a>
        </div>
        <div class="link-container main-mobile">
          <a>Pricing</a>
        </div>
        <div class="link-container main-mobile">
          <a>Company</a>
        </div>
        <div class="link-container">
          <a>Our Story</a>
        </div>
        <div class="link-container">
          <a class="hiring">Join the Team</a>
        </div>
        <div class="link-container">
          <a>Block</a>
        </div>
      </div>
      <!--<div class="col-3" style="padding-left: 4%">
        <div class="row" style="border: 0px; padding: 2px">
          <div
            class="col-9"
            style="
              font-weight: bold;
              padding-top: 15px;
              text-indent: 20px;
              font-size: 13pt;
            "
          >
            Press
          </div>
          <div class="col-3 text-align-center" style="height: 55px">
            <img src="/img/btn-arrow.svg" />
          </div>
        </div>
        <div class="row justify-center">
          <div style="border: 1px solid #eec69e; width: 90%" />
        </div>
        <div class="row" style="border: 0px; padding: 2px; margin-top: 20px">
          <div
            class="col-9"
            style="
              font-weight: bold;
              padding-top: 15px;
              text-indent: 20px;
              font-size: 13pt;
            "
          >
            Investor Relations
          </div>
          <div class="col-3 text-align-center" style="height: 55px">
            <img src="/img/btn-arrow.svg" />
          </div>
        </div>
        <div class="row justify-center">
          <div style="border: 1px solid #eec69e; width: 90%" />
        </div>
        <div
          class="row"
          style="
            border: 0px;
            background-color: #ffffff;
            box-shadow: -2px 3px 8px #e0b083;
            padding: 2px;
            border-radius: 30px;
            margin-top: 30px;
          "
        >
          <div
            class="col-9"
            style="
              font-weight: bold;
              padding-top: 15px;
              text-indent: 20px;
              font-size: 13pt;
            "
          >
            Get in Touch
          </div>
          <div
            class="button button-solid col-3 text-align-center"
            style="height: 55px"
          >
            <img src="/img/btn-arrow.svg" />
          </div>
        </div>
      </div>-->
    </div>
  </div>
</template>
<script>
import HoverButton from 'components/landingPage/HoverButton'
export default {
  components: {
    HoverButton
  },
  methods: {
    getInTouchButtonClicked() {}
  }
}
</script>
<style lang="scss" scoped>
.new::after {
  content: 'NEW';
  font-size: 8pt;
  font-weight: bold;
  margin-left: 15px;
  background-color: #eec69e;
  padding: 5px 10px;
  border-radius: 15px;
}
.hiring::after {
  content: 'WE`RE HIRING';
  font-size: 8pt;
  font-weight: bold;
  margin-left: 15px;
  background-color: #eec69e;
  padding: 5px 10px;
  border-radius: 15px;
}
.link-container {
  padding: 5px 0px 20px 10px;
}
.main,
.main-mobile {
  font-weight: bold;
}
.main {
  padding-bottom: 45px;
}
a {
  text-decoration: none;
  font-size: 13pt;
  clear: both;
  cursor: pointer;
}
</style>
