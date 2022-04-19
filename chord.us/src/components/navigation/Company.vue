<template>
  <div
    style="
      background-color: #ffffff;
      height: auto;
      border-radius: 0px 0px 25px 25px;
      padding-bottom: 50px;
    "
  >
    <div
      style="
        margin: 0px 40px 40px 40px;
        background-color: #f9f1e5;
        border-radius: 25px;
      "
    >
      <div style="padding: 40px 40px 0px 40px">
        <div style="font-size: 17pt; font-weight: bold">
          <span> The Company </span>
          <span style="float: right; cursor: pointer" @click="hideEvent">
            Close Nav
          </span>
        </div>
      </div>
      <div
        style="
          background-color: #f8f0e4;
          border-radius: 25px;
          color: #0a1f44;
          padding-bottom: 6vw;
          margin: 50px 0px;
        "
      >
        <div class="row">
          <div v-for="card in cards" :key="card.step" class="company-card">
            <div
              :id="`step-company-${card.step}`"
              class=""
              style="
                margin: 0px 40px 0px 30px;
                padding: 5px 0px;
                border-radius: 25px;
                cursor: pointer;
              "
              @mouseover="activateCard(true)"
              @mouseout="activateCard(false)"
            >
              <div style="margin: 45px 60px">
                <span v-show="card.step" class="company-steps">
                  {{ card.step }}
                </span>
                <span
                  v-show="card.nonStep"
                  class="company-steps"
                  style="border: 0px"
                >
                  {{ card.nonStep }}
                </span>
                <div class="company-divider" />
                <div v-if="card.step != '04'" class="company-header">
                  {{ card.header }}
                </div>
                <div v-if="card.step != '04'" class="company-description">
                  {{ card.description }}
                </div>
                <div
                  v-if="card.step != '04'"
                  :id="`button-company-${card.step}`"
                  class="button"
                  style="margin-top: 60px; width: 65%"
                >
                  Learn More
                  <img src="/img/btn-arrow.svg" />
                </div>
                <div v-if="card.step == '04'" style="padding-left: 4%">
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
                  <div
                    class="row"
                    style="border: 0px; padding: 2px; margin-top: 20px"
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
                  <div style="font-weight: bold; margin-top: 25px">
                    &#169; CoudEngage Inc. 2020
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    hideEvent: { type: Function, required: true }
  },
  data() {
    return {
      activeCard: 'transparent',
      activeButton: '',
      cards: [
        {
          step: '01',
          header: 'Our Story',
          description:
            "Since 2013, we've worked tirelessly to personalize the digital universe."
        },
        {
          step: '02',
          header: 'Join the Team',
          description:
            'CloudEngage is growing hyper-fast, building the most intuitive personalization ecosystem in the world.'
        },
        {
          step: '03',
          header: 'Blog',
          description: 'Full Spectrum Personalization. A blog.'
        },
        {
          step: '04'
        }
      ]
    }
  },
  methods: {
    activateCard(active) {
      let cardElement = event.target
      let cardElementId = ''
      while (!cardElement.id) {
        cardElement = cardElement.parentNode
      }
      cardElementId = cardElement.id.split('-')[2]
      document.getElementById(
        'step-company-' + cardElementId
      ).className = active ? 'active' : ''
      document.getElementById(
        'button-company-' + cardElementId
      ).className = active ? 'button button-solid' : 'button'
    }
  }
}
</script>

<style lang="scss" scoped>
.active {
  background-color: #ffffff;
}
.company-card {
  width: 25%;
}

.company-steps {
  padding: 9px;
  border: 1px solid #eec69e;
  font-size: 17pt;
  font-weight: bold;
  border-radius: 8px;
}

.company-divider {
  border: 1px solid #007fa9;
  clear: both;
  width: 95px;
  margin: 4vw 0 1.1vw 0;
}

.company-header {
  font-size: 27pt;
  font-weight: bold;
}

.company-description {
  margin-top: 1vw;
  font-size: 13pt;
  font-weight: bold;
  line-height: 28px;
  height: 110px;
}

.company-card-url {
  font-weight: bold;
  color: #007fa9;
  font-size: 13pt;
}
</style>
