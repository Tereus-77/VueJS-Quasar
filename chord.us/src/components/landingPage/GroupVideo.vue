<template>
  <div
    class="row full-width"
    style="
      background-color: #fffcf5;
      margin-top: 0px;
      background-image: url(/img/landingPage/logo-bg-dotted.svg);
      background-position: 65% top;
      background-size: 60%;
      background-repeat: no-repeat;
      height: auto;
      margin-top: 65px;
    "
  >
    <WatchVideosTogether />
    <EnterRoom />
    <Experience />
  </div>
</template>

<script>
import WatchVideosTogether from '../landingPage/WatchVideosTogether.vue'
import EnterRoom from '../landingPage/EnterRoom.vue'
import Experience from '../landingPage/Experience.vue'
export default {
  name: 'PageIndex',
  components: {
    WatchVideosTogether,
    EnterRoom,
    Experience
  }
}
</script>
