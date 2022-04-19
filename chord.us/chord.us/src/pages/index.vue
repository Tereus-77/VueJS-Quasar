<template>
  <q-page class="flex flex-center" style="overflow-x: hidden">
    <Carousel />
    <IntroChordVideo />
    <QuickStart />
    <GroupVideo />
    <WantMore />
  </q-page>
</template>

<script>
import Carousel from 'components/landingPage/Carousel.vue'
import IntroChordVideo from 'components/landingPage/IntroChordVideo.vue'
import QuickStart from 'components/landingPage/QuickStart.vue'
import GroupVideo from 'components/landingPage/GroupVideo.vue'
import WantMore from 'components/landingPage/WantMore.vue'
export default {
  name: 'PageIndex',
  components: {
    Carousel,
    IntroChordVideo,
    QuickStart,
    GroupVideo,
    WantMore
  }
}
</script>
