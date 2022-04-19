<template>
  <div id="content-element-container">
    <div class="carousel-card-bg carousel-card-bg-4 mobile-hide"></div>
    <div class="carousel-card-bg carousel-card-bg-3 mobile-hide"></div>
    <div class="carousel-card-bg carousel-card-bg-2 mobile-hide"></div>
    <div class="carousel-card-bg carousel-card-bg-1 mobile-hide">
      <div
        class="mobile-hide"
        style="
          width: 52vw;
          height: 52vw;
          position: absolute;
          float: right;
          right: -2.75vw;
          top: 35px;
          z-index: 0;
          clip-path: polygon(0 0, 94.65% 0, 94.65% 100%, 0% 100%);
        "
      ></div>
      <img v-if="slideImage.length" :src="slideImage" :class="imageClass" />
      <img
        src="/img/landingPage/powered-by-ce-white.png"
        class="powered-by-logo-desktop position-absolute float-right"
        style="margin: 35px 0"
      />
    </div>
    <div class="carousel-left mobile-hide">
      <div class="slide-index">
        <span class="light-color font-circStdBold fs-14 ls-4">
          {{ slideIndexNumber }}
        </span>
        <div class="separator"></div>
        <span class="light-color font-circStdBold fs-14 ls-4">
          {{ slideIndexLabel }}
        </span>
      </div>
      <div
        class="slide-title light-color"
        style="
          margin-top: 117px;
          font-size: 3.5vw;
          line-height: 3.5vw;
          max-width: 650px;
        "
      >
        {{ slideTitle }}
      </div>
      <div
        class="slide-body light-color mobile-hide"
        style="
          font-size: 14pt;
          font-weight: bold;
          margin-top: 20px;
          max-width: 550px;
        "
      >
        {{ slideBody }}
      </div>
      <div class="row" style="margin-top: 45px">
        <BasicButton
          button-text="Learn More"
          use-border
          :on-click="learnMoreButtonClicked"
          icon="/img/btn-arrow.svg"
          font-color-class="light-color"
          style="width: 270px"
        />
        <BasicButton
          v-if="slideIndex == 0"
          button-text="Get a Demo"
          use-background
          color="#007FA9"
          :on-click="demoButtonClicked"
          style="margin-left: 40px; width: 267px"
        />
        <BasicButton
          v-else-if="slideIndex == 1"
          button-text="Get Started"
          use-background
          color="#007FA9"
          :on-click="getStartedButtonClicked"
          style="margin-left: 40px; width: 267px"
        />
      </div>
      <div class="row">
        <div
          v-if="slideIndex == 0 || slideIndex == 1"
          style="
            margin-left: 0px;
            margin-top: 23px;
            width: 582px;
            height: 60px;
            padding: 0px;
          "
          class="button button-outline col-12"
        >
          <div class="row" style="margin-top: 2px">
            <div class="col-5">
              <q-input
                borderless
                label="Your email address"
                style="
                  text-color: #ffffff;
                  margin-left: 20px;
                  font-family: CircularStdBook;
                "
              />
            </div>
            <div class="col-1" />
            <div class="col-6">
              <!--<BasicButton
                button-text="Sign Up"
                use-background
                on-click="signupButtonClicked"
                style="width: 100%"
              />-->
              <div
                class="button button-solid text-align-center"
                style="margin-left: 20px; width: 267px; height: 52px"
                @click="signupButtonClicked"
              >
                Sign Up
                <img
                  src="/img/btn-arrow.svg"
                  class="left-margin"
                  style="bottom: -4px"
                />
              </div>
            </div>
          </div>
        </div>
        <div
          v-else-if="slideIndex == 1"
          style="margin: 23px 0px; max-width: 582px; height: 60px; padding: 0px"
          class="col-12"
        >
          <div class="row" style="margin-top: 2px">
            <div class="col-12">
              <p class="font-circStdBook dark-color fs-13 text-align-left">
                Download the app:
              </p>
              <div class="">
                <img src="/img/carousel/app-store-badge.png" class="badge" />
                <img src="/img/carousel/play-store-badge.png" class="badge" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="carousel-left-mobile desktop-hide position-relative">
      <div class="bg-circle-mobile"></div>
      <div class="slide-index">
        <span class="light-color font-circStdBold position-relative fs-14 ls-4">
          {{ slideIndexNumber }}
        </span>
        <div class="separator"></div>
        <span class="light-color font-circStdBold position-relative fs-14 ls-4">
          {{ slideIndexLabel }}
        </span>
      </div>
      <div
        class="slide-title light-color"
        style="
          margin-top: 50px;
          font-size: 44px;
          line-height: 48px;
          width: 100%;
        "
      >
        {{ slideTitle }}
      </div>
      <div
        class="slide-body light-color"
        style="
          font-size: 14pt;
          font-weight: bold;
          margin-top: 20px;
          max-width: 100%;
        "
      >
        {{ slideBody }}
      </div>
      <div class="row" style="margin-top: 45px">
        <BasicButton
          button-text="Learn More"
          use-border
          :on-click="learnMoreButtonClicked"
          icon="/img/btn-arrow.svg"
          font-color-class="light-color"
          style="width: 45%"
        />
        <BasicButton
          v-if="slideIndex == 0"
          button-text="Get a Demo"
          use-background
          color="#007FA9"
          :on-click="demoButtonClicked"
          style="margin-left: 40px; width: 45%"
        />
        <BasicButton
          v-else-if="slideIndex == 1"
          button-text="Get Started"
          use-background
          color="#007FA9"
          :on-click="getStartedButtonClicked"
          style="margin-left: 40px; width: 270px"
        />
      </div>
      <div class="row">
        <div
          v-if="slideIndex == 0 || slideIndex == 1"
          style="
            margin-left: 0px;
            margin-top: 23px;
            width: 582px;
            height: 60px;
            padding: 0px;
          "
          class="button button-outline col-12"
        >
          <div class="row" style="margin-top: 2px">
            <div class="col-5">
              <q-input
                v-model="signupEmailAddress"
                borderless
                label="Your email address"
                color="primary"
                style="margin-left: 20px; font-family: CircularStdBook"
              />
            </div>
            <div class="col-1" />
            <div class="col-6 items-end">
              <!--<BasicButton
                button-text="Sign Up"
                use-background
                on-click="signupButtonClicked"
                style="width: 100%"
              />-->
              <div
                class="button button-solid float-right text-align-center"
                style="height: 52px; width: 70%; margin-right: 2px"
                @click="signupButtonClicked"
              >
                Sign Up
                <img
                  src="/img/btn-arrow.svg"
                  class="left-margin"
                  style="bottom: -4px"
                />
              </div>
            </div>
          </div>
        </div>
        <div
          v-else-if="slideIndex == 1"
          style="margin: 23px 0px; max-width: 582px; height: 60px; padding: 0px"
          class="col-12"
        >
          <div class="row" style="margin-top: 2px">
            <div class="col-12">
              <p class="font-circStdBook dark-color fs-13 text-align-left">
                Download the app:
              </p>
              <div class="">
                <img src="/img/carousel/app-store-badge.png" class="badge" />
                <img src="/img/carousel/play-store-badge.png" class="badge" />
              </div>
            </div>
          </div>
        </div>
        <div
          class="row desktop-hide position-relative"
          style="margin-top: 25px"
        >
          <div class="col-12">
            <img
              v-if="slideImage.length"
              :src="slideImage"
              class="mobile-slide-img"
              :class="imageClass"
            />
            <img
              src="/img/landingPage/powered-by-ce-white.png"
              class="powered-by-logo float-right"
              style="margin: 35px 0"
            />
          </div>
        </div>
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
  props: {
    slideTitle: { type: String, required: true },
    slideBody: { type: String, required: true },
    slideImage: { type: String, required: false, default: '' },
    slideIndex: { type: Number, required: true },
    slideIndexLabel: { type: String, required: true }
  },
  data() {
    return {
      viewSignupModal: false,
      signupEmailAddress: ''
    }
  },
  computed: {
    imageClass() {
      return 'slide' + this.slideIndex
    },
    slideIndexNumber() {
      return '0' + (this.slideIndex + 1)
    }
  },
  methods: {
    demoButtonClicked() {},
    learnMoreButtonClicked() {},
    getStartedButtonClicked() {},
    signupButtonClicked() {
      console.log('signup button clicked - ' + this.signupEmailAddress)
      this.$refs['signupModal'].showModal = true
      //this.$refs['signupModal'].email = this.$refs['signupEmailAddress'].val
    }
  }
}
</script>
<style scoped>
.carousel-left-mobile {
  height: fit-content;
  overflow: hidden;
  background-color: #1c3a66;
  border-radius: 8px;
  width: 90%;
  padding: 20px;
}

.slide-title {
  font-family: CircularStdBold;
}

.slide-body {
  font-family: CircularStdBold;
}

.separator {
  height: 2px;
  width: 80px;
  display: inline-block;
  background-color: var(--ce-color);
  vertical-align: middle;
  margin: 0 15px 3px 15px;
}

.mobile-slide-img {
  left: 65%;
  bottom: 225px;
}

.badge {
  width: 120px;
  height: 40px;
  cursor: pointer;
}

.badge:first-of-type {
  margin-right: 10px;
}

.bg-circle-mobile {
  width: 70vw;
  height: 70vw;
  position: absolute;
  left: 50%;
  bottom: 5vw;
  transform: translateX(-50%);
  z-index: 0;
  border-radius: 35vw;
  background-color: #324d75;
}

.powered-by-logo {
  bottom: 20px;
  right: 15px;
}

.powered-by-logo-desktop {
  bottom: 100px;
  right: 35px;
}

.powered-by-logo,
.powered-by-logo-desktop {
  width: 156px;
  height: 35px;
}
</style>

<style>
.q-carousel input.q-field__native {
  color: #ffffff;
}
.q-carousel div.q-field__label {
  color: #ffffff;
}
</style>
