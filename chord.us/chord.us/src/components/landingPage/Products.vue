<template>
  <div
    class="full-width mobile-hide"
    style="margin-top: 3vw; padding-bottom: 2vw"
  >
    <div style="background-color: transparent">
      <div class="row">
        <div
          style="
            color: #ffffff;
            margin-top: 14vw;
            font-size: 27pt;
            font-weight: bold;
            width: 50%;
            line-height: 2.5vw;
            padding: 0vw 6vw 0vw 12.5vw;
          "
        >
          Customer Engagement products that your team and customers will ❤️ love
        </div>
        <div
          style="
            color: rgb(255, 255, 255);
            margin-top: 14vw;
            font-size: 18pt;
            width: 50%;
            line-height: 1.95vw;
            padding: 0.5vw 11vw 0vw 5vw;
          "
        >
          CloudEngage builds software that enables you to engage customers to
          drive conversion and lower costs. We make our customer lives better
          with intuitive and easy to use software. Our products help your
          marketing, support and sales deliver the incredible customer
          experiences.
        </div>
      </div>
      <div style="border-radius: 25px; color: #0a1f44; padding-bottom: 6vw">
        <div class="row" style="padding: 0vw 0vw 6vw 12vw">
          <div v-for="card in cards" :key="card.step" class="p-card">
            <span class="p-icon">
              <img :src="`${card.icon}`" />
            </span>
            <div class="p-divider" />
            <div class="row">
              <div class="col-7">
                <div class="p-header">
                  {{ card.product }}
                </div>
                <div class="p-description">
                  {{ card.description }}
                </div>
              </div>
              <div class="col-5">
                <div>
                  <div
                    class="button button-outline p-button"
                    @mouseover="activeButton(true)"
                    @mouseout="activeButton(false)"
                  >
                    {{ card.button }}
                  </div>
                  <div class="p-button-sub">
                    <span
                      @mouseover="activeSubButton(true)"
                      @mouseout="activeSubButton(false)"
                    >
                      {{ card.buttonSub }}
                    </span>
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
  data() {
    return {
      cards: [
        {
          icon: '/img/landingPage/generic-icon.svg',
          product: 'Personalization',
          description: 'Intituitive, affordable and powerful personalization',
          button: 'Start Trial',
          buttonSub: 'Schedule a Demo'
        },
        {
          icon: '/img/landingPage/generic-icon.svg',
          product: 'AIM',
          description: 'Customer Data Platform',
          button: 'Start Today',
          buttonSub: 'Free Forever'
        },
        {
          icon: '/img/landingPage/generic-icon.svg',
          product: 'Chord',
          description: 'Machine Learning Powered Live Chat',
          button: 'Start Trial',
          buttonSub: 'Schedule a Demo'
        },
        {
          icon: '/img/landingPage/answerdash-icon.svg',
          product: 'AnswerDash',
          description: 'AI Powered Self-Service',
          button: 'Sign Up Now',
          buttonSub: 'Schedule a Demo'
        },
        {
          icon: '/img/landingPage/chord-video-bg-element-plain.svg',
          product: 'Chord Video',
          description: 'Ground-breaking Video Conferencing & Chat',
          button: 'Buy Now',
          buttonSub: 'Schedule a Demo'
        },
        {
          icon: '/img/landingPage/chord-connect-icon.svg',
          product: 'Chord Connect',
          description: 'Intituitive, affordable and powerful personalization',
          button: 'Learn More',
          buttonSub: 'Schedule a Demo'
        }
      ]
    }
  },
  methods: {
    activeButton(hover) {
      event.target.className =
        'button button-outline p-button ' + (hover ? 'p-active' : '')
    },
    activeSubButton(hover) {
      event.target.parentNode.className =
        'p-button-sub' + (hover ? '-hover' : '')
    }
  }
}
</script>

<style lang="scss" scoped>
.p-card {
  width: 49%;
  padding-top: 5vw;
  height: 17vw;
  padding-right: 10vw;
}

.p-icon {
  width: 75px;
  height: 75px;
}

.p-divider {
  border: 1px solid #007fa9;
  width: 18vw;
  margin: -2.55vw 0 0 8.5vw;
}

.p-header {
  font-size: 17pt;
  font-weight: bold;
  color: #ffffff;
  margin: 3.75vw 0vw 0vw 0.25vw;
}

.p-description {
  margin-top: 1vw;
  font-size: 13pt;
  font-weight: bold;
  color: #bbc0c1;
  padding-right: 35px;
}

.p-card-url {
  font-weight: bold;
  color: #007fa9;
  font-size: 13pt;
}

.p-button {
  color: #ffffff;
  margin-top: 4vw;
  text-align: center;
}

.p-button-sub {
  color: #eec69e !important;
  text-align: center;
  font-size: 14pt;
  margin-top: 1.25vw;
  cursor: pointer;
}

.p-button-sub span {
  border-bottom: 1px solid #eec69e;
}

.p-button-sub-hover {
  cursor: pointer;
  color: #ffffff !important;
  text-align: center;
  font-size: 14pt;
  margin-top: 1.25vw;
}

.p-button-sub-hover span {
  border-bottom: 0px solid #eec69e !important;
}

.p-active {
  background-color: #eec69e;
  color: #0a1f44 !important;
  border-color: #eec69e !important;
}
</style>
