<template>
  <div class="row full-width" style="height: auto">
    <div class="col-3 mobile-hide" style="z-index: 1">
      <div
        style="
          background-image: url(/img/landingPage/quick-start-asset-left.png);
          background-repeat: no-repeat;
          background-position: right;
          background-size: 150% 80%;
          width: 115%;
          height: 105%;
          margin-top: 3.75vw;
          margin-left: 0vw;
        "
      />
    </div>
    <div class="col-6 mobile-hide position-relative" style="z-index: 1">
      <div class="row">
        <img
          src="/img/landingPage/chord-video-bg-element.svg"
          class="position-absolute"
          style="top: 20px; left: 50%; transform: translateX(-50%)"
        />
      </div>
      <div
        class="row justify-center"
        style="
          font-size: 43pt;
          font-weight: bold;
          margin-top: 7.5vw;
          line-height: 3.5vw;
          text-align: center;
        "
      >
        Experience the new
        <br />
        era of group video.
      </div>
      <div class="row justify-center" style="margin-top: 2vw">
        <div
          style="
            margin-left: 0px;
            margin-top: 0px;
            width: 582px;
            height: 60px;
            padding: 0px;
          "
          class="button button-outline col-12"
        >
          <div class="row justify-between" style="margin-top: 2px">
            <div class="col-5">
              <q-input
                borderless
                label="Your email address"
                style="margin-left: 20px"
              />
            </div>
            <div class="col-1" />
            <!--<div
              class="button button-solid col-5 text-align-center"
              style="margin-left: 20px; width: 267px; height: 52px"
            >
              Sign up
              <img
                src="/img/btn-arrow.svg"
                class="left-margin"
                style="bottom: -4px"
              />
            </div>-->
            <BasicButton
              button-text="Sign Up"
              use-background
              :on-click="signupButtonClicked"
              style="width: 267px; margin-right: 1px"
            />
          </div>
        </div>
      </div>
      <div
        class="row full-width justify-center q-pa-lg"
        style="font-weight: bold; font-size: 14pt"
      >
        or
      </div>
      <div class="row full-width justify-center">
        <!--<div
          class="button button-solid col-7 text-align-center"
          style="width: 14vw"
        >
          Get a Demo
          <img src="/img/btn-arrow.svg" />
        </div>-->
        <BasicButton
          button-text="Get a Demo"
          use-background
          color="#007FA9"
          :on-click="demoButtonClicked"
          style="width: 267px"
        />
      </div>
    </div>
    <div class="col-3 mobile-hide" style="z-index: 1">
      <div
        style="
          background-image: url(/img/landingPage/quick-start-asset.png);
          background-repeat: no-repeat;
          background-size: 150% 80%;
          width: 114%;
          height: 105%;
          margin-top: 6.5vw;
          margin-left: -3.5vw;
          z-index: 1;
        "
      />
    </div>
    <div
      class="col-12 position-relative desktop-hide"
      style="height: 130vw; width: 100vw"
    >
      <div class="position-absolute bg-circle-mobile"></div>
      <img
        src="/img/landingPage/quick-start-asset-left.png"
        class="experience-image-top-mobile"
      />
      <img
        src="/img/landingPage/quick-start-asset.png"
        class="experience-image-btm-mobile"
      />
      <div class="experience-block items-center">
        <img
          src="/img/landingPage/chord-video-bg-element.svg"
          class="experience-icon-mobile"
        />
        <div
          class="row justify-center text-center fs-36 font-circStdBold experience-text"
        >
          Experience the <br />
          new era <br />
          of group video.
        </div>
        <div
          class="row justify-center"
          style="margin: 2vw 15px; position: relative"
        >
          <div
            style="
              margin-left: 0px;
              margin-top: 0px;
              width: 90%;
              height: 60px;
              padding: 0 2px;
            "
            class="button button-outline col-12"
          >
            <div class="row justify-between" style="margin-top: 2px">
              <div class="col-6">
                <q-input
                  borderless
                  label="Your email address"
                  style="margin-left: 20px"
                />
              </div>
              <BasicButton
                button-text="Sign Up"
                use-background
                :on-click="signupButtonClicked"
                style="width: 150px; margin-right: 1px"
              />
            </div>
          </div>
        </div>
        <div
          class="row full-width justify-center q-pa-lg"
          style="font-weight: bold; font-size: 14pt"
        >
          or
        </div>
        <div class="row full-width justify-center">
          <BasicButton
            button-text="Get a Demo"
            use-background
            color="#007FA9"
            :on-click="demoButtonClicked"
            style="width: 267px"
          />
        </div>
      </div>
    </div>
    <div class="full-width" style="z-index: 0">
      <div
        class="mobile-hide"
        style="
          border: 75px solid #eed3b7;
          border-radius: 50%;
          width: 54vw;
          height: 54vw;
          margin: auto;
          margin-top: -36vw;
        "
      />
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
    return {}
  },
  methods: {
    demoButtonClicked() {},
    signupButtonClicked() {
      this.$refs['signupModal'].showModal = true
    }
  }
}
</script>
<style scoped>
.bg-circle-mobile {
  border: 35px solid #eed3b7;
  border-radius: 50%;
  width: 130vw;
  height: 130vw;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  z-index: 0;
}
.experience-block {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;
}
.experience-text {
  line-height: 44px;
  margin: 20px 0;
}
.experience-icon-mobile {
  position: relative;
  left: 50%;
  transform: translateX(-50%);
}
.experience-image-top-mobile,
.experience-image-btm-mobile {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  width: 373px;
  height: 223px;
}
.experience-image-top-mobile {
  top: -150px;
}
.experience-image-btm-mobile {
  bottom: -150px;
}
</style>
