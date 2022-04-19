<template>
  <div id="intro-chord-video" class="full-width justify-center">
    <div style="position: absolute">
      <img
        src="/img/landingPage/opera-logo.svg"
        class="mobile-hide"
        style="margin-top: 150px; margin-left: 27.75vw; width: 70px"
      />
      <img
        src="/img/landingPage/opera-logo.svg"
        class="desktop-hide"
        style="margin-top: 75px; margin-left: 17.75vw; width: 70px"
      />
    </div>
    <div style="position: absolute">
      <img
        src="/img/landingPage/opera-logo.svg"
        class="mobile-hide"
        style="margin-top: 425px; margin-left: 86.25vw; width: 28px"
      />
      <img
        src="/img/landingPage/opera-logo.svg"
        class="desktop-hide"
        style="margin-top: 425px; margin-left: 86.25vw; width: 28px"
      />
    </div>
    <div style="position: absolute">
      <img
        src="/img/landingPage/firefox-logo.svg"
        class="mobile-hide"
        style="margin-top: 365px; margin-left: 19.75vw; width: 70px"
      />
      <img
        src="/img/landingPage/firefox-logo.svg"
        class="desktop-hide"
        style="margin-top: 365px; margin-left: 19.75vw; width: 70px"
      />
    </div>
    <div style="position: absolute">
      <img
        src="/img/landingPage/firefox-logo.svg"
        class="mobile-hide"
        style="margin-top: 75px; margin-left: 66.9vw; width: 25px"
      />
      <img
        src="/img/landingPage/firefox-logo.svg"
        class="desktop-hide"
        style="margin-top: 75px; margin-left: 66.9vw; width: 25px"
      />
    </div>
    <div style="position: absolute">
      <img
        src="/img/landingPage/chrome-logo.svg"
        class="mobile-hide"
        style="margin-top: 415px; margin-left: 72.25vw; width: 75px"
      />
      <img
        src="/img/landingPage/chrome-logo.svg"
        class="desktop-hide"
        style="margin-top: 315px; margin-left: 72.25vw; width: 75px"
      />
    </div>
    <div style="position: absolute">
      <img
        src="/img/landingPage/safari-logo.svg"
        style="margin-top: 130px; margin-left: 84.5vw; width: 75px"
      />
    </div>
    <div style="position: absolute">
      <img
        src="/img/landingPage/safari-logo.svg"
        style="margin-top: 590px; margin-left: 39vw; width: 27px"
      />
    </div>
    <div
      class="intro-block mobile-hide"
      style="max-width: 600px; margin: auto; margin-top: 100px; height: 430px"
    >
      <div class="text-align-center">
        <img src="/img/landingPage/chord-video-bg-element-beige.svg" />
      </div>
      <div
        class="text-align-center fs-28 position-relative"
        style="margin-top: 47px"
      >
        Introducing
      </div>
      <div
        class="text-align-center fs-47 font-circStdBold position-relative"
        style="line-height: 78px"
      >
        ChordVideo
      </div>
      <div
        class="text-align-center fs-16 position-relative"
        style="margin-top: 47px"
      >
        Browser based for your convenience. Does your team use different
        browsers? Mac or PC? Doesn't matter, <span>we support it all.</span>
      </div>
    </div>
    <div
      class="intro-block-mobile desktop-hide"
      style="max-width: 600px; margin: auto; height: 430px"
    >
      <div class="text-align-center">
        <img src="/img/landingPage/chord-video-bg-element-beige.svg" />
      </div>
      <div
        class="text-align-center fs-28 position-relative"
        style="margin-top: 47px"
      >
        Introducing
      </div>
      <div
        class="text-align-center fs-47 font-circStdBold position-relative"
        style="line-height: 78px"
      >
        ChordVideo
      </div>
      <div
        class="text-align-center fs-16 position-relative"
        style="margin-top: 47px"
      >
        Browser based for your convenience. Does your team use different
        browsers? Mac or PC? Doesn't matter, <span>we support it all.</span>
      </div>
    </div>
    <img
      src="/img/landingPage/intro-chord-video-asset.png"
      class="position-relative intro-chord-bottom mobile-hide"
    />
    <div class="position-relative intro-chord-bottom desktop-hide mobile" />
  </div>
</template>

<style lang="scss" scoped>
#intro-chord-intro {
  min-height: 100px;
  width: 100%;
  border: 1px solid black;
}
.intro-chord-bottom {
  width: 100%;
  margin-top: 20px;
}

.intro-chord-bottom.mobile {
  background: url(/img/landingPage/intro-chord-video-asset.png);
  background-size: cover;
  background-repeat: no-repeat;
  height: 200px;
  background-position-x: center;
}
</style>
