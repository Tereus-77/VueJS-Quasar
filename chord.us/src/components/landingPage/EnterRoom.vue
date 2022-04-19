<template>
  <div class="full-width" style="padding-top: 12vw">
    <main class="padding-y-xl">
      <div class="container margin-bottom-lg">
        <ul class="stack-cards js-stack-cards mobile-hide">
          <li
            v-for="(card, index) in cards"
            :key="index"
            class="stack-cards__item bg radius-lg js-stack-cards__item"
            style="height: 500px"
          >
            <div class="row no-wrap">
              <div class="col-5">
                <div style="max-width: 500px; margin: 0 auto">
                  <div class="card-title">
                    {{ card.title }}
                  </div>
                  <div class="card-body" style="">
                    {{ card.body }}
                  </div>
                  <div class="card-step ce-color">
                    <hr class="card-hr" />
                    Step {{ getCardIndex(index) }}
                  </div>
                  <div class="card-lower-body vertical-bottom">
                    {{ card.lowerBody }}
                  </div>
                </div>
              </div>
              <div class="col-7">
                <img
                  :src="`/img/landingPage/step-${card.step}-asset.png`"
                  class="card-image"
                />
              </div>
            </div>
          </li>
        </ul>
        <div class="desktop-hide">
          <ul class="step-list-mobile">
            <li
              class="cardIndex card0"
              :class="selectedCardIndex == 0 ? 'active' : ''"
              @click="setActiveCard(0)"
            >
              Step 01
            </li>
            <li
              class="cardIndex card1"
              :class="selectedCardIndex == 1 ? 'active' : ''"
              @click="setActiveCard(1)"
            >
              Step 02
            </li>
            <li
              class="cardIndex card2"
              :class="selectedCardIndex == 2 ? 'active' : ''"
              @click="setActiveCard(2)"
            >
              Step 03
            </li>
          </ul>
          <div v-for="(card, index) in cards" :key="index" class="col-12">
            <div
              :class="selectedCardIndex == index ? '' : 'hidden'"
              style="padding: 5vw"
            >
              <!--<div class="card-title-mobile">
                {{ card.title }}
              </div>
              <div class="card-body-mobile" style="">
                {{ card.body }}
              </div>-->
              <div class="card-lower-body-mobile vertical-bottom">
                {{ card.lowerBody }}
              </div>
            </div>
          </div>
        </div>
        <ul class="stack-cards js-stack-cards desktop-hide">
          <li
            v-for="(card, index) in cards"
            :key="index"
            class="stack-cards__item-mobile bg radius-lg"
            :class="selectedCardIndex == index ? '' : 'hidden'"
            style="height: 400px"
          >
            <div class="col-12">
              <img src="/img/landingPage/step-3-asset.png" class="card-image" />
            </div>
          </li>
        </ul>
      </div>
    </main>
  </div>
</template>
<script>
export default {
  data() {
    return {
      element: null,
      items: [],
      scrollingFn: false,
      scrolling: false,
      selectedCardIndex: 0,
      cards: [
        {
          title: 'Want to enter a breakout room during your call?',
          body:
            'Our clean-sheet approach examined the worst of current video chat. A key area our team focused on is simple workflows for busy presenters. This makes it casual and easy to see everyone, and easily go into breakout rooms and return to the group video chat at the end.',
          lowerBody: 'Start your 1:1 and jump back and forth.',
          step: 1
        },
        {
          title: 'Want to enter a breakout room during your call?',
          body:
            'Our clean-sheet approach examined the worst of current video chat. A key area our team focused on is simple workflows for busy presenters. This makes it casual and easy to see everyone, and easily go into breakout rooms and return to the group video chat at the end.',
          lowerBody: 'Start your 1:1 and jump back and forth.',
          step: 2
        },
        {
          title: 'Want to enter a breakout room during your call?',
          body:
            'Our clean-sheet approach examined the worst of current video chat. A key area our team focused on is simple workflows for busy presenters. This makes it casual and easy to see everyone, and easily go into breakout rooms and return to the group video chat at the end.',
          lowerBody: 'Start your 1:1 and jump back and forth.',
          step: 3
        }
      ]
    }
  },
  mounted() {
    let that = this
    this.$nextTick(() => {
      var StackCards = function (element) {
        that.element = element
        that.items = that.element.getElementsByClassName('js-stack-cards__item')
        that.scrollingFn = false
        that.scrolling = false
        that.initStackCardsEffect(that)
        that.initStackCardsResize(that)
      }
      // eslint-disable-next-line no-unused-vars
      var stackCards = document.getElementsByClassName('js-stack-cards'),
        // eslint-disable-next-line no-unused-vars
        intersectionObserverSupported =
          'IntersectionObserver' in window &&
          'IntersectionObserverEntry' in window &&
          'intersectionRatio' in window.IntersectionObserverEntry.prototype,
        // eslint-disable-next-line no-unused-vars
        reducedMotion = this.osHasReducedMotion()
      if (
        stackCards.length > 0 &&
        intersectionObserverSupported &&
        !reducedMotion
      ) {
        var stackCardsArray = []
        for (var i = 0; i < stackCards.length; i++) {
          ;(function (i) {
            stackCardsArray.push(new StackCards(stackCards[i]))
          })(i)
        }
      }
      var resizingId = false,
        // eslint-disable-next-line no-unused-vars
        customEvent = new CustomEvent('resize-stack-cards')
      window.addEventListener('resize', function () {
        clearTimeout(resizingId)
        resizingId = setTimeout(this.doneResizing, 500)
      })
    })
  },
  methods: {
    setActiveCard(index) {
      var that = this
      var x = document.getElementsByClassName('cardIndex')
      var i
      for (i = 0; i < x.length; i++) {
        x[i].classList.remove('active')
        if (i == index) {
          x[i].classList.add('active')
          that.selectedCardIndex = index
        }
      }
    },
    getCardIndex(index) {
      return index + 1
    },
    osHasReducedMotion() {
      if (!window.matchMedia) return false
      var matchMediaObj = window.matchMedia('(prefers-reduced-motion: reduce)')
      if (matchMediaObj) return matchMediaObj.matches
      return false // return false if not supported
    },
    initStackCardsEffect(element) {
      console.log('initializing stack effect')
      // use Intersection Observer to trigger animation
      this.setStackCards(element) // store cards CSS properties
      var observer = new IntersectionObserver(
        this.stackCardsCallback.bind(element),
        { threshold: [0, 1] }
      )
      observer.observe(element.element)
    },
    stackCardsCallback(entries) {
      // Intersection Observer callback
      if (entries[0].isIntersecting) {
        if (this.scrollingFn) return // listener for scroll event already added
        this.stackCardsInitEvent(this)
      } else {
        if (!this.scrollingFn) return // listener for scroll event already removed
        window.removeEventListener('scroll', this.scrollingFn)
        this.scrollingFn = false
      }
    },
    stackCardsInitEvent(element) {
      element.scrollingFn = this.stackCardsScrolling.bind(element)
      window.addEventListener('scroll', element.scrollingFn)
    },
    stackCardsScrolling() {
      if (this.scrolling) return
      this.scrolling = true
      window.requestAnimationFrame(this.animateStackCards.bind(this))
    },
    initStackCardsResize(element) {
      // detect resize to reset gallery
      element.element.addEventListener('resize-stack-cards', function () {
        this.setStackCards(element)
        this.animateStackCards.bind(element)
      })
    },
    setStackCards(element) {
      // store wrapper properties
      element.marginY = getComputedStyle(element.element).getPropertyValue(
        '--stack-cards-gap'
      )
      this.getIntegerFromProperty(element) // convert element.marginY to integer (px value)
      element.elementHeight = element.element.offsetHeight

      // store card properties
      var cardStyle = getComputedStyle(element.items[0])
      element.cardTop = Math.floor(
        parseFloat(cardStyle.getPropertyValue('top'))
      )
      element.cardHeight = Math.floor(
        parseFloat(cardStyle.getPropertyValue('height'))
      )

      // store window property
      element.windowHeight = window.innerHeight

      // reset margin + translate values
      if (isNaN(element.marginY)) {
        element.element.style.paddingBottom = '0px'
      } else {
        element.element.style.paddingBottom =
          element.marginY * (element.items.length - 1) + 'px'
      }

      for (var i = 0; i < element.items.length; i++) {
        if (isNaN(element.marginY)) {
          element.items[i].style.transform = 'none;'
        } else {
          element.items[i].style.transform =
            'translateY(' + element.marginY * i + 'px)'
        }
      }
    },
    getIntegerFromProperty(element) {
      var node = document.createElement('div')
      node.setAttribute(
        'style',
        'opacity:0; visbility: hidden;position: absolute; height:' +
          element.marginY
      )
      element.element.appendChild(node)
      element.marginY = parseInt(
        getComputedStyle(node).getPropertyValue('height')
      )
      element.element.removeChild(node)
    },
    animateStackCards() {
      if (isNaN(this.marginY)) {
        // --stack-cards-gap not defined - do not trigger the effect
        this.scrolling = false
        return
      }

      var top = this.element.getBoundingClientRect().top
      if (Math.abs(top) - (this.elementHeight - this.cardHeight) > 0) {
        this.scrolling = false
        return
      }

      for (var i = 0; i < this.items.length; i++) {
        // use only scale
        var scrolling =
          this.cardTop - top - i * (this.cardHeight + this.marginY)
        if (scrolling > 0) {
          var marginY = scrolling + 100 * i
          var scaling =
            i == this.items.length - 1
              ? 1
              : (this.cardHeight - scrolling * 0.05) / this.cardHeight
          this.items[i].style.transform =
            'translateY(' + marginY + 'px) scale(' + scaling + ')'
        } else {
          this.items[i].style.transform = 'translateY(' + 100 * i + 'px)'
        }
      }

      this.scrolling = false
    },
    doneResizing() {
      for (var i = 0; i < this.stackCardsArray.length; i++) {
        ;(function (i) {
          this.stackCardsArray[i].element.dispatchEvent(this.customEvent)
        })(i)
      }
    }
  }
}
</script>
<style scoped>
.bg {
  background-color: #fffcf5 !important;
}

.card-title {
  font-size: 43pt;
  font-weight: bold;
  margin-top: 50px;
  line-height: 60px;
  max-width: 700px;
}

.card-hr {
  width: 95%;
  border-top: 1px solid #eed3b7;
  margin: 25px 0 35px 0;
}

.card-body {
  font-size: 14pt;
  margin-top: 27px;
  max-width: 500px;
}

.card-lower-body {
  font-size: 27pt;
  font-weight: bold;
  max-width: 350px;
  margin-top: 20px;
}

.card-title-mobile {
  font-size: 43pt;
  font-weight: bold;
  margin-top: 50px;
  line-height: 60px;
  max-width: 700px;
}

.card-body-mobile {
  font-size: 14pt;
  margin-top: 27px;
  max-width: 500px;
}

.card-lower-body-mobile {
  font-size: 27pt;
  font-weight: bold;
  max-width: 350px;
}

.card-image {
  width: 100%;
  /*position: absolute;*/
}

.step-list-mobile {
  display: inline-block;
  width: 100%;
  margin-left: 5vw;
}

.step-list-mobile li {
  display: inline;
  margin-right: 15px;
  color: #e0b083;
  line-height: 24px;
  font-size: 16px;
}

.step-list-mobile li.active {
  color: var(--ce-color);
}
</style>
