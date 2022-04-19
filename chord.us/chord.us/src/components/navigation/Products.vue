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
          <span> CloudEngage Products </span>
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
          <div v-for="card in cards" :key="card.step" class="product-card">
            <div
              :id="`step-${card.step}`"
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
                <span v-show="card.step" class="product-steps">
                  {{ card.step }}
                </span>
                <span
                  v-show="card.nonStep"
                  class="product-steps"
                  style="border: 0px"
                >
                  {{ card.nonStep }}
                </span>
                <div class="product-divider" />
                <div class="product-header">
                  {{ card.header }}
                </div>
                <div class="product-description">
                  {{ card.description }}
                </div>
                <div
                  :id="`button-${card.step}`"
                  class="button"
                  style="margin-top: 60px; width: 65%"
                >
                  Learn More
                  <img src="/img/btn-arrow.svg" />
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
          header: 'Chord Video',
          description:
            'This is an introductory sentence, consectetur adipiscing elit, sed do incididunt ut labore et dolore mangna aliqua.'
        },
        {
          step: '02',
          header: 'Chord Chat',
          description:
            'This is an introductory sentence, consectetur adipiscing elit, sed do incididunt ut labore et dolore mangna aliqua.'
        },
        {
          step: '03',
          header: 'Personalization',
          description:
            'This is an introductory sentence, consectetur adipiscing elit, sed do incididunt ut labore et dolore mangna aliqua.'
        },
        {
          step: '04',
          header: 'AnswerDash',
          description:
            'This is an introductory sentence, consectetur adipiscing elit, sed do incididunt ut labore et dolore mangna aliqua.'
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
      cardElementId = cardElement.id.split('-')[1]
      document.getElementById('step-' + cardElementId).className = active
        ? 'active'
        : ''
      document.getElementById('button-' + cardElementId).className = active
        ? 'button button-solid'
        : 'button'
    }
  }
}
</script>

<style lang="scss" scoped>
.active {
  background-color: #ffffff;
}
.product-card {
  width: 25%;
}

.product-steps {
  padding: 9px;
  border: 1px solid #eec69e;
  font-size: 17pt;
  font-weight: bold;
  border-radius: 8px;
}

.product-divider {
  border: 1px solid #007fa9;
  clear: both;
  width: 95px;
  margin: 4vw 0 1.1vw 0;
}

.product-header {
  font-size: 27pt;
  font-weight: bold;
}

.product-description {
  margin-top: 1vw;
  font-size: 13pt;
  font-weight: bold;
  line-height: 28px;
}

.product-card-url {
  font-weight: bold;
  color: #007fa9;
  font-size: 13pt;
}
</style>
