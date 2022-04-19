<template>
  <div
    class="row full-width"
    style="height: 50px; height: auto; padding-top: 100px"
  >
    <div
      style="
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 90%;
        z-index: -1;
      "
    ></div>
    <div
      style="
        margin-left: 31.5vw;
        width: 68vw;
        background-color: #eed3b7;
        border-radius: 20px 0px 0px 20px;
        padding: 6vw;
      "
    >
      <div
        :style="`
          background-color: #ffffff;
          margin-top: -1vw;
          margin-left: ${$q.platform.is.desktop ? '-27.5vw' : '-33.5vw'};
          width: ${$q.platform.is.desktop ? '83vw' : '92vw'};
          border-radius: 20px;
          z-index: 1;
          padding: 4vw 4vw 6.5vw 4vw;
        `"
      >
        <SimpleReliable />
        <MakeItYours />
      </div>
    </div>
  </div>
</template>

<script>
import MakeItYours from '../landingPage/MakeItYours.vue'
import SimpleReliable from '../landingPage/SimpleReliable.vue'
export default {
  name: 'PageIndex',
  components: {
    MakeItYours,
    SimpleReliable
  }
}
</script>
