<template>
  <div class="row">
    <div class="col-5 mobile-hide" style="">
      <div class="" style="max-width: 350px; margin: 0 auto">
        <div style="color: #858c8d; font-size: 17pt">
          <img
            src="/img/landingPage/quick-start-icon.svg"
            class="quick-start-icon"
          />
          Quick Start
        </div>
        <div
          style="
            font-size: 43pt;
            font-weight: bold;
            margin-top: 95px;
            line-height: 60px;
          "
        >
          Simple.
          <br />
          Reliable.
        </div>
        <div style="font-size: 14pt; margin-top: 27px; max-width: 350px">
          Chord Community powered by ChordVideo breathes real-life into virtual.
          It can be better than in-person when it’s done right.
        </div>
        <div class="row" style="margin-top: 45px">
          <BasicButton
            button-text="Get a Demo"
            use-background
            color="#007FA9"
            :on-click="demoButtonClicked"
          />
          <BasicButton
            button-text="Sign Up"
            color="#007FA9"
            font-color-class="ce-color"
            icon="/img/ce-arrow.svg"
            rotate-icon
            :on-click="signupButtonClicked"
          />
        </div>
      </div>
    </div>
    <div class="col-7 mobile-hide">
      <img
        src="/img/landingPage/simple-reliable-image.png"
        style="width: 55vw; position: absolute; margin-left: -1vw"
      />
    </div>
    <div class="col-12 desktop-hide">
      <div style="color: #858c8d; margin-top: 5.5vw; font-size: 17pt">
        <img
          src="/img/landingPage/quick-start-icon.svg"
          class="quick-start-icon"
        />
        Quick Start
      </div>
      <div class="simple-title">Simple. Reliable.</div>
      <div
        class="col-12 desktop-hide position-relative"
        style="min-height: 300px; margin-top: 20px"
      >
        <div class="quick-start-img-wrapper">
          <img
            src="/img/landingPage/placeholder2.png"
            style="width: 100%; position: absolute; margin: 0 auto"
          />
        </div>
      </div>
      <div
        style="font-size: 14pt; font-family: CircularStdBold; margin-top: 27px"
      >
        Chord Community powered by ChordVideo breathes real-life into virtual.
        It can be better than in-person when it’s done right.
      </div>
      <div class="row" style="margin-top: 45px">
        <BasicButton
          button-text="Get a Demo"
          use-background
          color="#007FA9"
          :on-click="demoButtonClicked"
        />
        <BasicButton
          button-text="Sign Up"
          color="#007FA9"
          font-color-class="ce-color"
          icon="/img/ce-arrow.svg"
          rotate-icon
          :on-click="signupButtonClicked"
        />
      </div>
    </div>
    <SignupModal ref="signupModal" />
  </div>
</template>
<script>
import BasicButton from 'components/landingPage/BasicButton'
import SignupModal from 'components/SignupModal'
export default {
  components: {
    BasicButton,
    SignupModal
  },
  data() {
    return {
      showSignupModal: false
    }
  },
  methods: {
    demoButtonClicked() {},
    signupButtonClicked() {
      console.log('signup button clicked')
      this.$refs['signupModal'].showModal = true
    }
  }
}
</script>
<style scoped>
.quick-start-img-wrapper {
  width: 100%;
  height: 100%;
  position: absolute;
  left: 50%;
  bottom: 0;
  transform: translateX(-50%);
}
.quick-start-icon {
  display: inline-block;
  margin-right: 10px;
  width: 24px;
  height: 26px;
  vertical-align: sub;
}

.simple-title {
  margin-top: 95px;
  line-height: 60px;
  font-size: 36px;
  font-family: CircularStdBold;
}
</style>
