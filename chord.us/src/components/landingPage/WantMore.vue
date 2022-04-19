<template>
  <div class="full-width q-pa-xl" style="margin-top: 5.5vw">
    <div
      class="mobile-hide"
      style="background-color: #007fa9; border-radius: 25px"
    >
      <div
        style="
          font-size: 40pt;
          color: #ffffff;
          padding-top: 6.75vw;
          font-weight: bold;
          padding-left: 20vw;
        "
      >
        Want more?
        <div style="font-size: 14pt; font-weight: bold; margin-top: 1vw">
          Well fantastic, Chord Video comes jam-
          <br />
          packed with features:
        </div>
      </div>
      <div
        style="
          background-color: #f8f0e4;
          margin: 2.5vw 15vw 0vw 12vw;
          border-radius: 25px;
          color: #0a1f44;
          padding-bottom: 6vw;
        "
      >
        <div class="row" style="padding: 0vw 0vw 5vw 8vw">
          <div v-for="card in cards" :key="card.step" class="wm-card">
            <span v-show="card.step" class="wm-steps">
              {{ card.step }}
            </span>
            <span
              v-show="card.nonStep"
              class="wm-steps-plain"
              style="border: 0px"
            >
              {{ card.nonStep }}
            </span>
            <div class="wm-divider" />
            <div class="wm-header">
              {{ card.header }}
            </div>
            <div class="wm-description">
              {{ card.description }}
            </div>
            <a v-show="card.linkUrl" class="wm-card-url">{{ card.linkText }}</a>
            <div v-if="card.descriptionCont" class="wm-description-cont">
              {{ card.descriptionCont }}
            </div>
          </div>
        </div>
      </div>
      <div
        style="
          background-color: #0a1f44;
          margin: -1vw 3.5vw;
          border-radius: 25px;
        "
      >
        <Products />
      </div>
    </div>
    <div
      class="desktop-hide"
      style="
        background-color: #007fa9;
        border-radius: 25px;
        padding-bottom: 15px;
      "
    >
      <div
        style="
          font-size: 40pt;
          color: #ffffff;
          padding-top: 15px;
          font-weight: bold;
          padding-left: 15px;
          margin-top: 100px;
        "
      >
        Want more?
        <div style="font-size: 14pt; margin-top: 1vw">
          Well fantastic, Chord Video comes <br />
          jam-packed with features:
        </div>
      </div>
      <div
        style="
          background-color: #f8f0e4;
          margin: 10px 15px 0px 15px;
          border-radius: 25px;
          color: #0a1f44;
          padding: 15px;
        "
      >
        <div class="row" style="padding-bottom: 15px">
          <div v-for="card in cards" :key="card.step" class="wm-card-mobile">
            <span v-show="card.step" class="wm-steps-mobile">
              {{ card.step }}
            </span>
            <span
              v-show="card.nonStep"
              class="wm-steps-mobile special"
              style="border: 0px"
            >
              {{ card.nonStep }}
            </span>
            <div class="wm-divider-mobile" />
            <div class="wm-header-mobile">
              {{ card.header }}
            </div>
            <div class="wm-description mobile">
              {{ card.description }}
            </div>
            <a v-show="card.linkUrl" class="wm-card-url">{{ card.linkText }}</a>
          </div>
        </div>
      </div>
      <div
        style="
          background-color: #0a1f44;
          margin: -1vw 3.5vw;
          border-radius: 25px;
        "
      >
        <Products />
      </div>
    </div>
  </div>
</template>

<script>
import Products from '../landingPage/Products.vue'
export default {
  components: {
    Products
  },
  data() {
    return {
      cards: [
        {
          step: '01',
          header: 'Easy to Use',
          description:
            'Delightful workflows that get people into sales appointments, meetings and conferences.'
        },
        {
          step: '02',
          header: 'Scale',
          description:
            'Large-scale for hundreds and even thousands of attendees.'
        },
        {
          step: '03',
          header: 'Customization',
          description:
            'Deep customization available via enterprise, including creating mind-blowing bespoke experiences for.'
        },
        {
          step: '04',
          header: 'Anytime',
          description:
            "Chord Chat to Video let's you start from a chat conversation and either schedule an appointment or immediately connect via video."
        },
        {
          step: '05',
          header: 'Personal Chat',
          description:
            'Fast login with your mobile device or email, and then you can easily send DMs and chat. You can even schedule video chats and share images and video in chat.'
        },
        {
          step: '06',
          header: 'Breakout',
          description:
            'Start big, go small and focused, and then return to the primary video chat with a few taps. Breathe, it doesn’t need to be so difficult.'
        },
        {
          step: '07',
          header: 'HD Simulcast',
          description:
            'Powered by CloudEngage, you can easily watch video together. Everyone experiences the same feeling, as every beat matches and the group experiences it at the exact same time.'
        },
        {
          step: '08',
          header: 'Scheduler',
          description:
            'You’re not always ready to virtually sell. With scheduler, not only can visitors make a sales appointment, but we’ve created workflows to help them make that meeting.'
        },
        {
          nonStep: '🎉',
          linkText: 'Sign up for free.',
          linkUrl: 'https://cloudengage.com',
          header: 'And More!',
          description: "Don't miss out!",
          descriptionCont:
            'Chord Community is the best way to transform an inperson business to virtual.  Period.'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.wm-card {
  width: 33.33%;
  padding-top: 4vw;
  height: fit-content;
  padding-right: 10%;
}

.wm-card-mobile {
  width: 100%;
  padding: 12px;
  height: fit-content;
  margin-bottom: 30px;
}

.wm-steps {
  padding: 9px;
  border: 1px solid #eec69e;
  background-color: #fff;
  font-size: 17pt;
  font-weight: bold;
  border-radius: 8px;
}

.wm-steps-mobile {
  padding: 2px 2px 4px 5px;
  border: 1px solid #eec69e;
  background-color: #fff;
  font-size: 17pt;
  font-weight: bold;
  border-radius: 8px;
  display: inline-block;
  width: 40px;
  height: 40px;
  vertical-align: bottom;
}

.wm-steps-mobile.special {
  padding-left: 9px;
  padding-top: 4px;
}

.wm-steps-plain {
  padding: 9px;
  font-size: 17pt;
}

.wm-divider {
  width: 95px;
  margin: 2.3vw 0 1.1vw 0;
}

.wm-divider,
.wm-divider-mobile {
  border: 1px solid #007fa9;
  clear: both;
}

.wm-divider-mobile {
  height: 40px;
  width: 1;
  margin: 0 2.3vw;
  display: inline-block;
  vertical-align: middle;
}

.header-wrapper {
  display: inline-block;
}

.wm-header,
.wm-header-mobile {
  font-size: 27pt;
  font-weight: bold;
}

.wm-header-mobile {
  display: inline-block;
  line-height: 36px;
  vertical-align: middle;
}

.wm-description {
  margin-top: 1vw;
  font-size: 13pt;
}

.wm-description.mobile {
  margin-top: 20px;
  line-height: 24px;
}

.wm-description-cont {
  font-size: 13pt;
}

.wm-card-url {
  font-weight: bold;
  color: #007fa9;
  font-size: 13pt;
  cursor: pointer;
}
</style>
