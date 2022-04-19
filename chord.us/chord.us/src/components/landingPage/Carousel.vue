<template>
  <div style="width: 100%; height: fit-content">
    <q-carousel
      ref="carousel"
      v-model="slide"
      swipeable
      animated
      keep-alive
      infinite
      transition-prev="slide-right"
      transition-next="slide-left"
      :style="`height: ${carouselHeight}; width: 100%;`"
      @transition="onTransition"
    >
      <q-carousel-slide
        v-for="(cSlide, index) in slides"
        :key="index"
        :name="index"
      >
        <CarouselSlide
          :slide-title="cSlide.title"
          :slide-body="cSlide.body"
          :slide-image="cSlide.image"
          :slide-index="index"
          :slide-index-label="cSlide.indexLabel"
        />
      </q-carousel-slide>
      <template v-slot:control>
        <q-carousel-control
          position="bottom-left"
          :offset="[175, 120]"
          class="carousel-controls mobile-hide"
        >
          <q-bar class="text-align-center">
            <div class="cursor-pointer col-3">
              <div class="border-radius-right">
                <div
                  id="nav0"
                  class="carousel-control active"
                  @click="gotoSlide(0)"
                >
                  <div id="newLabel" class="new-label active">NEW</div>
                  Chord Video
                </div>
              </div>
            </div>
            <div class="cursor-pointer col-3">
              <div class="border-radius-right">
                <div id="nav1" class="carousel-control" @click="gotoSlide(1)">
                  Chord Chat
                </div>
              </div>
            </div>
            <div class="cursor-pointer col-3">
              <div class="border-radius-right">
                <div id="nav2" class="carousel-control" @click="gotoSlide(2)">
                  Personalization
                </div>
              </div>
            </div>
            <div class="cursor-pointer col-3">
              <div class="border-radius-right">
                <div id="nav3" class="carousel-control" @click="gotoSlide(3)">
                  AnswerDash
                </div>
              </div>
            </div>
          </q-bar>
        </q-carousel-control>
        <q-carousel-control
          position="bottom-left"
          :offset="[0, 0]"
          class="carousel-controls desktop-hide"
          style="width: 100%; border-radius: 10px 10px 0px 0px"
        >
          <q-bar class="text-align-center">
            <div class="carousel-nav-mobile" style="width: 25%">
              <div class="carousel-nav-mobile-item" @click="gotoSlide(0)">
                <svg
                  width="35px"
                  height="35px"
                  viewBox="0 0 53 59"
                  version="1.1"
                  style="margin: 6px 0px 0px 6px"
                  xmlns="http://www.w3.org/2000/svg"
                  xmlns:xlink="http://www.w3.org/1999/xlink"
                >
                  <title>chord-video-bg-element-plain</title>
                  <g
                    id="Page-1"
                    stroke="none"
                    stroke-width="1"
                    fill="none"
                    fill-rule="evenodd"
                    opacity="0.119999997"
                  >
                    <g
                      id="chord-video-lp-v2@2x"
                      transform="translate(-321.000000, -9925.000000)"
                      fill="#000000"
                    >
                      <g
                        id="Group-35"
                        transform="translate(118.000000, 8820.000000)"
                      >
                        <g
                          id="chord-video-bg-element-plain"
                          transform="translate(203.000000, 1105.000000)"
                        >
                          <path
                            id="Combined-Shape"
                            d="M-1.02274761e-11,38.680946 C0.463961973,39.050452 0.951122044,39.4013665 1.47539907,39.7081262 L1.47539907,39.7081262 L11.0446148,45.2390966 C13.3157086,46.554445 14.726153,49.0038747 14.726153,51.6299237 C14.726153,54.2559727 13.3157086,56.7054024 11.0469346,58.0184269 C8.77584071,59.3268035 5.95263211,59.3268035 3.68385806,58.0207508 C1.4104444,56.7054024 -1.02274761e-11,54.2559727 -1.02274761e-11,51.6299237 L-1.02274761e-11,51.6299237 Z M26.500348,32.0421548 L30.1818862,34.1685573 C31.8498295,35.1376391 33.100207,36.7643951 33.6082454,38.6421363 C33.7775915,39.2672754 33.8634245,39.9156538 33.8634245,40.5593844 C33.8634245,43.1854334 32.4529801,45.6348631 30.1818862,46.9478876 L30.1818862,46.9478876 L18.984164,53.4247003 C19.0769564,52.8367442 19.1372715,52.2348445 19.1372715,51.6306209 C19.1372715,47.4312665 16.8800965,43.5154324 13.249594,41.4169172 L13.249594,41.4169172 L11.6210875,40.4733987 C12.1778419,40.2549486 12.725317,40.0109352 13.249594,39.7088234 L13.249594,39.7088234 L26.500348,32.0421548 Z M45.6369235,22.1191757 C46.8965803,22.1191757 48.1353587,22.439879 49.2581467,23.069666 C49.279025,23.0836096 49.2999033,23.0975532 49.3207816,23.1091729 C50.9887248,24.0689589 52.2344627,25.6980389 52.7448209,27.5688082 C52.8863293,28.0893702 52.9605632,28.6633826 52.9768019,29.3187329 C52.9768019,29.3605638 52.9907208,29.4651409 53,29.5325351 C52.9837613,32.1423165 51.5779566,34.5661829 49.3231014,35.8745595 L49.3231014,35.8745595 L38.1253792,42.3583441 C38.1253792,42.3467244 38.127699,42.3374287 38.127699,42.3281329 C38.2019329,41.8424301 38.2436895,41.3497554 38.2599281,40.8152499 C38.2645677,40.7780669 38.2784866,40.5991237 38.2784866,40.5596168 L38.2784866,40.5596168 L38.273847,29.4907043 C38.2715272,26.8669792 39.6819716,24.4175495 41.9530654,23.0998772 C43.0619345,22.4561466 44.3355102,22.1191757 45.6369235,22.1191757 Z M0.000463961965,16.5398674 C0.464425935,16.9140213 0.949266196,17.2626119 1.47586303,17.5693716 L1.47586303,17.5693716 L22.0896935,29.493493 L15.8494049,33.1002434 C15.8331663,33.1095391 15.8169276,33.1188349 15.8030087,33.1281306 L15.8030087,33.1281306 L11.0450787,35.8796722 C9.92925018,36.5234028 8.65567456,36.8673455 7.36354047,36.8673455 C6.68615599,36.8673455 5.94845645,36.7348811 5.11564471,36.4699522 C4.63312426,36.3119245 4.12276609,36.1376292 3.6773626,35.8819961 C1.40858855,34.5643238 0.000463961965,32.117218 0.000463961965,29.493493 L0.000463961965,29.493493 Z M22.8171859,12.0372392 C25.0882797,10.7265387 27.9091685,10.7265387 30.1825822,12.0372392 L30.1825822,12.0372392 L41.3687053,18.5047563 C40.8003519,18.7208824 40.2575164,18.9788394 39.7448384,19.2763034 C36.1166558,21.3771426 33.8618006,25.2906527 33.8641204,29.492331 L33.8641204,29.492331 L33.8641204,31.3700722 C33.393199,30.9842986 32.9013993,30.6450038 32.3864015,30.3475399 L32.3864015,30.3475399 L11.6194636,18.3374328 C12.1298218,18.1375742 12.6262611,17.9075044 13.2247721,17.5844772 L13.2247721,17.5844772 L18.0592558,14.8724425 Z M3.6796824,0.96646755 C5.91597911,-0.323317556 8.81342163,-0.320993619 11.0450787,0.96646755 L11.0450787,0.96646755 L22.2404811,7.44328033 C21.6976456,7.6547586 21.1640893,7.898772 20.5725378,8.23341895 L20.5725378,8.23341895 L11.0450787,13.7411499 C8.81806125,15.0286111 5.9136593,15.0262872 3.6796824,13.7434739 L3.6796824,13.7434739 C1.41090836,12.4304494 0.000463961964,9.98101967 0.000463961964,7.35264678 C0.000463961964,4.72659782 1.41090836,2.27949203 3.6796824,0.96646755 Z"
                          ></path>
                        </g>
                      </g>
                    </g>
                  </g>
                </svg>
              </div>
              Chord Video
            </div>
            <div class="carousel-nav-mobile" style="width: 25%">
              <div class="carousel-nav-mobile-item" @click="gotoSlide(1)">
                <div
                  style="
                    margin: 3px auto;
                    width: 42px;
                    height: 42px;
                    background-color: rgba(0, 0, 0, 0.09);
                    border-radius: 30px;
                  "
                />
              </div>
              Chord Chat
            </div>
            <div
              class="carousel-nav-mobile"
              style="width: 25%"
              @click="gotoSlide(2)"
            >
              <div class="carousel-nav-mobile-item">
                <div
                  style="
                    margin: 3px auto;
                    width: 42px;
                    height: 42px;
                    background-color: rgba(0, 0, 0, 0.09);
                    border-radius: 30px;
                  "
                />
              </div>
              Personalization
            </div>
            <div
              class="carousel-nav-mobile"
              style="width: 25%"
              @click="gotoSlide(3)"
            >
              <div class="carousel-nav-mobile-item">
                <svg
                  width="40px"
                  height="40px"
                  viewBox="0 0 63 52"
                  style="padding: 2px; margin-top: 3px"
                  version="1.1"
                  xmlns="http://www.w3.org/2000/svg"
                  xmlns:xlink="http://www.w3.org/1999/xlink"
                >
                  <title>answerdash-icon</title>
                  <g
                    id="Page-1"
                    stroke="none"
                    stroke-width="1"
                    fill="none"
                    fill-rule="evenodd"
                    opacity="0.119999997"
                  >
                    <g
                      id="chord-video-lp-v2@2x"
                      transform="translate(-933.000000, -9630.000000)"
                      fill="#000000"
                    >
                      <g
                        id="Group-35"
                        transform="translate(118.000000, 8820.000000)"
                      >
                        <g
                          id="answerdash-icon"
                          transform="translate(815.000000, 810.000000)"
                        >
                          <path
                            id="Fill-24"
                            d="M23.6139823,29.5000914 C19.58542,29.9444707 13.8857048,31.3435754 9.10849871,33.354277 L39.3447053,0.0217331684 C24.0241,0.455373798 8.72855179,11.8236106 4.89891184,25.7942026 C3.92782274,29.3369648 3.79231004,32.7089298 4.36862253,35.7812327 C3.20423607,36.5135127 0.710802448,38.4654069 1.65808394e-13,40.2863907 C8.77355223,36.3958979 19.5849086,34.0594544 30.8871789,34.0594544 C35.5667136,34.0594544 39.9409611,34.4624129 43.9352618,35.2069657 L36.7070657,15.0667107 L23.6139823,29.5000914 Z"
                          ></path>
                          <path
                            id="Fill-26"
                            d="M40.2504415,2.01658857e-14 C40.2427709,2.01658857e-14 40.2356118,0.000511368668 40.2279412,0.000511368668 C40.1404972,0.000511368668 40.0530532,0.00613642401 39.9656091,0.00664779268 L53.5925614,37.9747486 C53.876371,38.0887838 54.1744989,38.193103 54.4511494,38.3117406 C57.7346476,34.6027836 60.2147856,30.3420599 61.4615024,25.793947 C65.3663136,11.5482386 55.869686,2.01658857e-14 40.2504415,2.01658857e-14"
                          ></path>
                          <path
                            id="Fill-29"
                            d="M26.1098705,51.5883542 C32.9003351,51.5883542 39.7240386,49.3971394 45.5955736,45.7587513 C47.2012712,45.8364794 48.7609457,45.8421044 50.2807333,45.7792061 C50.8596027,45.7551718 51.2753454,45.382384 51.4159718,44.9339137 C45.2238086,41.9101907 36.5786099,40.046252 26.7122628,40.046252 C19.8906048,40.046252 13.1640613,40.9385903 7.06598997,42.4870146 C10.727901,48.049683 17.4759219,51.5883542 26.1098705,51.5883542"
                          ></path>
                        </g>
                      </g>
                    </g>
                  </g>
                </svg>
              </div>
              AnswerDash
            </div>
          </q-bar>
          <div class="carousel-nav-mobile-bottom"></div>
        </q-carousel-control>
      </template>
    </q-carousel>
  </div>
</template>

<script>
import CarouselSlide from '../carousel/slide.vue'

export default {
  name: 'Carousel',
  components: {
    CarouselSlide
  },
  data() {
    return {
      slide: 0,
      carouselHeight: 'auto',
      slides: [
        {
          title: 'Introducing, Chord Video.',
          body:
            'Browser-based, brand-forward gorgeous and easy-to-use video chat with simulcast video.',
          image: '/img/carousel/hero-chord-video-asset.png',
          indexLabel: 'CHORD VIDEO'
        },
        {
          title: 'Personalization, Meet Chat.',
          body:
            'Our clean sheet approach combines personalization with agent-driven live chat. No other platform combines this level of simplicity and sophistication.',
          image: '/img/carousel/chord-chat-image.png',
          indexLabel: 'CHORD CONNECT'
        },
        {
          title: 'Customer Journery Platform.',
          body: 'Intuitive, affordable and powerful personalization.',
          image: '/img/carousel/chord-video-asset.png',
          indexLabel: 'PERSONALIZATION'
        },
        {
          title: 'Ut lobortis tellus nec nisl tristique.',
          body:
            'Morbi non odio felis. Ut interdum dui eu erat hendrerit suscipit. Nullam sagittis nisi ut lectus vehicula, vitae posuere diam finibus.',
          image: '/img/carousel/answerdash-image.png',
          indexLabel: 'ANSWERDASH'
        }
      ]
    }
  },
  mounted() {
    this.carouselHeight = this.$q.platform.is.desktop ? '90vmax' : '105vmax'
  },
  methods: {
    gotoSlide(slide) {
      this.slide = slide
    },
    onTransition(newVal, oldVal) {
      let newLabelClasses = 'new-label'
      document
        .getElementById('nav' + oldVal)
        .setAttribute('class', 'carousel-control carousel-control')
      document
        .getElementById('nav' + newVal)
        .setAttribute('class', 'carousel-control carousel-control active')
      if (newVal == 0) {
        newLabelClasses += ' active'
      }
      document.getElementById('newLabel').setAttribute('class', newLabelClasses)
    }
  }
}
</script>
<style lang="sass" scoped>
#content-element-container
  transition: width .5s, height .5s
#video-element-container
  transition: width .5s, height .5s
.carousel-controls
  background-color: #FFFFFF
  border: 1px solid #007fa9
  border-radius: 15px
  width: calc(100% - 340px)
.new-label
  padding: 5px 10px
  margin: 0px 10px 5px 0px
  font-size: 10pt
  background-color: #007fa9
  border-radius: 20px
  color: #FFFFFF
  display: inline
.new-label.active
  background-color: #ffffff
  border-radius: 20px
  color: #0A1F44
.carousel-nav-mobile
  font-size: 8pt
  font-weight: bold
.carousel-nav-mobile-item
  margin: 10px auto !important
  width: 50px
  height: 50px
  border-radius: 50%
  border: 1px solid #E9E9E9
.carousel-nav-mobile-bottom
  width: 35%
  border: 3px solid #000000
  border-radius: 5px
  margin: 10px auto 5px
</style>
<style>
.q-carousel {
  max-height: 950px;
}
</style>
