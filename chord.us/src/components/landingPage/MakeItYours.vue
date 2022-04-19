<template>
  <div class="row" style="margin-top: 16vw">
    <div class="col-8 mobile-hide">
      <div style="position: absolute; padding: 10vw 8vw; z-index: 1">
        <div
          class="standup-outer-container"
          :style="`background-color: ${miyColor}`"
        >
          <div class="standup-inner-container">Standup</div>
          <div class="standup-date">
            <div class="row">
              <div class="col-1">
                <svg
                  width="20px"
                  height="20px"
                  viewBox="0 0 20 20"
                  version="1.1"
                  xmlns="http://www.w3.org/2000/svg"
                  xmlns:xlink="http://www.w3.org/1999/xlink"
                >
                  <title>calendar-icon</title>
                  <g
                    id="calendar-icon"
                    stroke="none"
                    stroke-width="1"
                    fill="none"
                    fill-rule="evenodd"
                  >
                    <path
                      id="Combined-Shape"
                      d="M5,0 L5,1.5 L15,1.5 L15,0 L17,0 L17,1.5 C18.6568542,1.5 20,2.84314575 20,4.5 L20,16.5 C20,18.1568542 18.6568542,19.5 17,19.5 L3,19.5 C1.34314575,19.5 0,18.1568542 0,16.5 L0,4.5 C0,2.84314575 1.34314575,1.5 3,1.5 L3,0 L5,0 Z M18,8 L2,8 L2,16.5 C2,17.0128358 2.38604019,17.4355072 2.88337887,17.4932723 L3,17.5 L17,17.5 C17.5128358,17.5 17.9355072,17.1139598 17.9932723,16.6166211 L18,16.5 L18,8 Z M15,12 C15.5522847,12 16,12.4477153 16,13 L16,15 C16,15.5522847 15.5522847,16 15,16 L12,16 C11.4477153,16 11,15.5522847 11,15 L11,13 C11,12.4477153 11.4477153,12 12,12 L15,12 Z M15,3.5 L5,3.5 L5,5 L3,5 L3,3.5 C2.48716416,3.5 2.06449284,3.88604019 2.00672773,4.38337887 L2,4.5 L2,6 L18,6 L18,4.5 C18,3.98716416 17.6139598,3.56449284 17.1166211,3.50672773 L17,3.5 L17,5 L15,5 L15,3.5 Z"
                      :fill="`${miyColor}`"
                      fill-rule="nonzero"
                    ></path>
                  </g>
                </svg>
              </div>
              <div class="col-1" />
              <div class="col-10" style="color: #8392a4; font-weight: normal">
                Meeting Date
              </div>
            </div>
            <div class="row" style="padding-top: 5px">
              <div class="col-1" />
              <div class="col-1" />
              <div class="col-10" style="font-weight: bold">
                September 18, 2020
              </div>
            </div>
            <div class="row" style="padding-top: 25px">
              <div class="col-1">
                <svg
                  width="20px"
                  height="20px"
                  viewBox="0 0 20 20"
                  version="1.1"
                  xmlns="http://www.w3.org/2000/svg"
                  xmlns:xlink="http://www.w3.org/1999/xlink"
                >
                  <title>time-icon</title>
                  <g
                    id="time-icon"
                    stroke="none"
                    stroke-width="1"
                    fill="none"
                    fill-rule="evenodd"
                  >
                    <path
                      id="Combined-Shape"
                      d="M10,0 C15.5228475,0 20,4.4771525 20,10 C20,15.5228475 15.5228475,20 10,20 C4.4771525,20 0,15.5228475 0,10 C0,4.4771525 4.4771525,0 10,0 Z M10,2 C5.581722,2 2,5.581722 2,10 C2,14.418278 5.581722,18 10,18 C14.418278,18 18,14.418278 18,10 C18,5.581722 14.418278,2 10,2 Z M10,5 C10.5128358,5 10.9355072,5.38604019 10.9932723,5.88337887 L11,6 L11,9.898 L14.6751801,13.2623471 C15.0512365,13.6065548 15.1039964,14.1720071 14.8165987,14.5773899 L14.7376529,14.6751801 C14.3934452,15.0512365 13.8279929,15.1039964 13.4226101,14.8165987 L13.3248199,14.7376529 L9,10.7791079 L9,6 C9,5.44771525 9.44771525,5 10,5 Z"
                      :fill="`${miyColor}`"
                      fill-rule="nonzero"
                    ></path>
                  </g>
                </svg>
              </div>
              <div class="col-1" />
              <div class="col-10" style="color: #8392a4; font-weight: normal">
                Time
              </div>
            </div>
            <div class="row" style="padding-top: 5px">
              <div class="col-1" />
              <div class="col-1" />
              <div class="col-10" style="font-weight: bold">11:30 - 12:30</div>
            </div>
          </div>
          <div class="text-align-center start-meeting">Start Meeting</div>
        </div>
        <div
          class="standup-details-outer"
          :style="`background-color: ${miyColor}`"
        >
          <div class="standup-details">
            <div class="row">
              <div class="col-3">
                <img
                  src="/img/landingPage/member-7.png"
                  style="width: 70px; border-radius: 10px"
                />
              </div>
              <div class="col-7">
                <div class="row" style="padding-top: 10px">
                  <div
                    class="col-12 q-pa-xs"
                    :style="`color: ${miyColor}; font-weight: bold;`"
                  >
                    Carlos Sarmiento
                  </div>
                </div>
                <div class="row">
                  <div
                    class="col-12 q-pa-xs"
                    style="color: #8392a4; font-weight: normal"
                  >
                    Context - Work, Personal
                  </div>
                </div>
              </div>
              <div class="col-2"></div>
            </div>
          </div>
          <div
            class="row"
            style="border: 1px solid #ececec; background-color: #f4f6f8"
          >
            <div class="col-6" style="border-right: 1px solid #ececec">
              <div class="row text-align-center">
                <div style="padding: 30px 30px 0px 30px; margin: auto">
                  <img src="/img/schedule-call-icon.svg" />
                </div>
              </div>
              <div class="row">
                <div
                  class="col text-align-center"
                  style="padding: 10px; color: #8d98a7"
                >
                  Schedule a Call
                </div>
              </div>
            </div>
            <div class="col-6" style="border-right: 1px solid #ececec">
              <div class="row text-align-center">
                <div style="padding: 30px 30px 0px 30px; margin: auto">
                  <img src="/img/request-breakout-icon.svg" />
                </div>
              </div>
              <div class="row">
                <div
                  class="col text-align-center"
                  style="padding: 10px; color: #8d98a7"
                >
                  Request 1:1 Breakout
                </div>
              </div>
            </div>
          </div>
          <div
            class="row"
            style="border: 1px solid #ececec; background-color: #f4f6f8"
          >
            <div class="col-6" style="border-right: 1px solid #ececec">
              <div class="row text-align-center">
                <div style="padding: 30px 30px 0px 30px; margin: auto">
                  <img src="/img/private-message-icon.svg" />
                </div>
              </div>
              <div class="row">
                <div
                  class="col text-align-center"
                  style="padding: 10px; color: #8d98a7"
                >
                  Send a Private Message
                </div>
              </div>
            </div>
            <div
              class="col-6"
              style="border-right: 1px solid #ececec; background-color: #ffffff"
            >
              <div class="row text-align-center">
                <div style="padding: 30px 30px 0px 30px; margin: auto">
                  <svg
                    width="22px"
                    height="22px"
                    viewBox="0 0 22 22"
                    version="1.1"
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                  >
                    <title>muted-icon</title>
                    <g
                      id="muted-icon"
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <path
                        id="Combined-Shape"
                        d="M17.5282275,3.54141657 C17.9088122,3.25232796 18.4480549,3.26498167 18.7965186,3.61344538 C19.1761299,3.99403004 19.1761299,4.61016839 18.7965186,4.9897797 L18.7965186,4.9897797 L13.7204341,10.0658642 L13.7204341,10.7306706 C13.7184874,12.6160735 12.1893352,14.1442523 10.3039324,14.146199 C10.0975796,14.146199 9.89706693,14.1199182 9.70142111,14.0848772 L9.70142111,14.0848772 L8.37472827,15.41157 C8.96750592,15.6656176 9.61965867,15.8077285 10.3039324,15.8077285 C13.0205866,15.8077285 15.2310924,13.5962493 15.2310924,10.8795951 L15.2310924,10.8795951 L15.2310924,10.5554654 C15.2310924,10.0181694 15.6681321,9.58210311 16.2044548,9.58210311 C16.7427241,9.58210311 17.1778171,10.0181694 17.1778171,10.5554654 L17.1778171,10.5554654 L17.1778171,10.8795951 C17.1778171,14.3389248 14.6071672,17.2015833 11.2772947,17.6765841 L11.2772947,17.6765841 L11.2772947,19.0266377 C11.2772947,19.5639337 10.8412284,20 10.3039324,20 C9.76566302,20 9.33057007,19.5639337 9.33057007,19.0266377 L9.33057007,19.0266377 L9.33057007,17.6765841 C8.46719769,17.5539405 7.65541352,17.2736121 6.92539178,16.8599332 L6.92539178,16.8599332 L4.1610428,19.6242821 C3.97123714,19.8150612 3.72205639,19.9094773 3.47287564,19.9094773 C3.22466825,19.9094773 2.97548749,19.8150612 2.78470848,19.6242821 C2.40509717,19.2446708 2.40509717,18.6285325 2.78470848,18.2479478 L2.78470848,18.2479478 L3.07963726,17.9539924 C3.1146783,17.9267383 3.15555952,17.9140846 3.18768048,17.8819636 L3.18768048,17.8819636 Z M4.40185263,9.58200578 C4.94012199,9.58200578 5.37521495,10.0180721 5.37521495,10.5553681 L5.37521495,10.5553681 L5.37521495,10.8794977 C5.37521495,11.4917426 5.49980533,12.0708932 5.70615814,12.6111093 L5.70615814,12.6111093 L4.22762078,14.0886733 C3.71855229,13.1308848 3.42849032,12.0387723 3.42849032,10.8794977 L3.42849032,10.8794977 L3.42849032,10.5553681 C3.42849032,10.0180721 3.86455663,9.58200578 4.40185263,9.58200578 Z M10.303835,2 C11.9381104,2 13.2988709,3.14856754 13.6366276,4.68063982 L13.6366276,4.68063982 L6.95254859,11.3647189 C6.91361409,11.158366 6.88733331,10.9471464 6.88733331,10.7300866 L6.88733331,10.7300866 L6.88733331,5.41650174 C6.88733331,3.5291522 8.41745888,2 10.303835,2 Z"
                        :fill="`${miyColor}`"
                      ></path>
                    </g>
                  </svg>
                </div>
              </div>
              <div class="row">
                <div
                  class="col text-align-center"
                  style="padding: 10px; color: #8d98a7"
                >
                  Mute Sean
                </div>
              </div>
            </div>
          </div>
          <div
            class="row"
            style="border: 1px solid #ececec; background-color: #f4f6f8"
          >
            <div class="col-6" style="border-right: 1px solid #ececec">
              <div class="row text-align-center">
                <div style="padding: 30px 30px 0px 30px; margin: auto">
                  <img src="/img/contact-details-icon.svg" />
                </div>
              </div>
              <div class="row">
                <div
                  class="col text-align-center"
                  style="padding: 10px; color: #8d98a7"
                >
                  Sean's Contact Details
                </div>
              </div>
            </div>
            <div class="col-6" style="border-right: 1px solid #ececec">
              <div class="row text-align-center">
                <div style="padding: 30px 30px 0px 30px; margin: auto">
                  <img src="/img/latency-icon.svg" />
                </div>
              </div>
              <div class="row">
                <div
                  class="col text-align-center"
                  style="padding: 10px; color: #8d98a7"
                >
                  Sean's Latency
                </div>
              </div>
            </div>
          </div>
          <div
            class="row"
            style="
              background-color: #ffffff;
              border-radius: 0px 0px 25px 25px;
              padding: 30px 5px;
            "
          >
            <div class="col-3 text-align-center">
              <img
                src="/img/landingPage/facebook-icon.svg"
                class="social-icon"
              />
            </div>
            <div class="col-3 text-align-center">
              <img
                src="/img/landingPage/linkedin-icon.svg"
                class="social-icon"
              />
            </div>
            <div class="col-3 text-align-center">
              <img
                src="/img/landingPage/twitter-icon.svg"
                class="social-icon"
              />
            </div>
            <div class="col-3 text-align-center">
              <img
                src="/img/landingPage/instagram-icon.svg"
                class="social-icon"
              />
            </div>
          </div>
          <div
            class="text-align-center"
            style="color: #ffffff; font-weight: bold; padding: 20px"
          >
            Close
          </div>
        </div>
      </div>
      <div
        :style="`
          width: 100%;
          background-color: ${miyBackgroundColor2};
          height: 63vw;
          border-radius: 25px;
        `"
      >
        <div
          :style="`
            width: 100px;
            height: 100px;
            border-radius: 25px;
            background-color: ${miyBackgroundColor1};
          `"
        >
          <div
            :style="`
              width: 52vw;
              height: 52vw;
              background-color: ${miyBackgroundColor1};
              top: -2.05vw;
              float: left;
              border-radius: 50%;
              left: -17vw;
              position: relative;
              clip-path: polygon(36% 4%, 100% 4%, 100% 100%, 36% 100%);
            `"
          ></div>
          <div
            :style="`
              width: 52vw;
              height: 52vw;
              background-color: ${miyBackgroundColor1};
              border-radius: 50%;
              clip-path: polygon(33% 7%, 100% 7%, 100% 100%, 33% 100%);
              margin-top: -54vw;
              float: left;
              left: -17.15vw;
              position: relative;
            `"
          ></div>
        </div>
      </div>
    </div>
    <div class="col-12 desktop-hide">
      <div class="fs-36 font-circStdBold">Make it Yours.</div>
      <div style="font-size: 14pt; margin: 27px 0">
        Currently stuck taking your meetings on unbranded third party apps with
        security issues? Is your brand poorly presented during a pitch?
        <span style="font-weight: bold">
          Your brand powered by Chord Video will move video chat from lame to
          great.
        </span>
      </div>
    </div>
    <div
      class="col-12 desktop-hide"
      style="position: relative; width: 120%; min-height: 420px"
    >
      <div
        style="
          position: absolute;
          padding: 45vw 4vw 0vw 3vw;
          z-index: 1;
          width: 100%;
        "
      >
        <div
          class="standup-outer-container-mobile"
          :style="`background-color: ${miyColor}`"
        >
          <div class="standup-inner-container">Standup</div>
          <div class="standup-date">
            <div class="row">
              <div class="col-1">
                <svg
                  width="10px"
                  height="10px"
                  viewBox="0 0 20 20"
                  version="1.1"
                  xmlns="http://www.w3.org/2000/svg"
                  xmlns:xlink="http://www.w3.org/1999/xlink"
                >
                  <title>calendar-icon</title>
                  <g
                    id="calendar-icon"
                    stroke="none"
                    stroke-width="1"
                    fill="none"
                    fill-rule="evenodd"
                  >
                    <path
                      id="Combined-Shape"
                      d="M5,0 L5,1.5 L15,1.5 L15,0 L17,0 L17,1.5 C18.6568542,1.5 20,2.84314575 20,4.5 L20,16.5 C20,18.1568542 18.6568542,19.5 17,19.5 L3,19.5 C1.34314575,19.5 0,18.1568542 0,16.5 L0,4.5 C0,2.84314575 1.34314575,1.5 3,1.5 L3,0 L5,0 Z M18,8 L2,8 L2,16.5 C2,17.0128358 2.38604019,17.4355072 2.88337887,17.4932723 L3,17.5 L17,17.5 C17.5128358,17.5 17.9355072,17.1139598 17.9932723,16.6166211 L18,16.5 L18,8 Z M15,12 C15.5522847,12 16,12.4477153 16,13 L16,15 C16,15.5522847 15.5522847,16 15,16 L12,16 C11.4477153,16 11,15.5522847 11,15 L11,13 C11,12.4477153 11.4477153,12 12,12 L15,12 Z M15,3.5 L5,3.5 L5,5 L3,5 L3,3.5 C2.48716416,3.5 2.06449284,3.88604019 2.00672773,4.38337887 L2,4.5 L2,6 L18,6 L18,4.5 C18,3.98716416 17.6139598,3.56449284 17.1166211,3.50672773 L17,3.5 L17,5 L15,5 L15,3.5 Z"
                      :fill="`${miyColor}`"
                      fill-rule="nonzero"
                    ></path>
                  </g>
                </svg>
              </div>
              <div class="col-1" />
              <div class="col-10" style="color: #8392a4; font-weight: normal">
                Meeting Date
              </div>
            </div>
            <div class="row" style="padding-top: 0px">
              <div class="col-1" />
              <div class="col-1" />
              <div class="col-10" style="font-weight: bold">
                September 18, 2020
              </div>
            </div>
            <div class="row" style="padding-top: 10px">
              <div class="col-1">
                <svg
                  width="10px"
                  height="10px"
                  viewBox="0 0 20 20"
                  version="1.1"
                  xmlns="http://www.w3.org/2000/svg"
                  xmlns:xlink="http://www.w3.org/1999/xlink"
                >
                  <title>time-icon</title>
                  <g
                    id="time-icon"
                    stroke="none"
                    stroke-width="1"
                    fill="none"
                    fill-rule="evenodd"
                  >
                    <path
                      id="Combined-Shape"
                      d="M10,0 C15.5228475,0 20,4.4771525 20,10 C20,15.5228475 15.5228475,20 10,20 C4.4771525,20 0,15.5228475 0,10 C0,4.4771525 4.4771525,0 10,0 Z M10,2 C5.581722,2 2,5.581722 2,10 C2,14.418278 5.581722,18 10,18 C14.418278,18 18,14.418278 18,10 C18,5.581722 14.418278,2 10,2 Z M10,5 C10.5128358,5 10.9355072,5.38604019 10.9932723,5.88337887 L11,6 L11,9.898 L14.6751801,13.2623471 C15.0512365,13.6065548 15.1039964,14.1720071 14.8165987,14.5773899 L14.7376529,14.6751801 C14.3934452,15.0512365 13.8279929,15.1039964 13.4226101,14.8165987 L13.3248199,14.7376529 L9,10.7791079 L9,6 C9,5.44771525 9.44771525,5 10,5 Z"
                      :fill="`${miyColor}`"
                      fill-rule="nonzero"
                    ></path>
                  </g>
                </svg>
              </div>
              <div class="col-1" />
              <div class="col-10" style="color: #8392a4; font-weight: normal">
                Time
              </div>
            </div>
            <div class="row" style="padding-top: 0px">
              <div class="col-1" />
              <div class="col-1" />
              <div class="col-10" style="font-weight: bold">11:30 - 12:30</div>
            </div>
          </div>
          <div
            class="text-align-center start-meeting"
            :style="`background-color: ${miyColor}`"
          >
            Start Meeting
          </div>
        </div>
        <div
          :style="`width: 52vw; background-color: ${miyColor}; border-radius: 5px; margin-top: -70vw; margin-left: 26vw`"
          class="desktop-hide big-box"
        >
          <div class="standup-details desktop-hide">
            <div class="row">
              <div class="col-3">
                <img
                  src="/img/landingPage/member-7.png"
                  style="width: 60px; border-radius: 5px"
                />
              </div>
              <div class="col-7">
                <div class="row" style="padding-top: 10px">
                  <div
                    class="col-12"
                    :style="`color: ${miyColor}; font-weight: bold; padding-left: 5px;`"
                  >
                    Carlos Sarmiento
                  </div>
                </div>
                <div class="row">
                  <div
                    class="col-12 q-pa-xs"
                    style="color: #8392a4; font-weight: normal; font-size: 6pt"
                  >
                    Context - Work, Personal
                  </div>
                </div>
              </div>
              <div class="col-2"></div>
            </div>
          </div>
          <div
            class="row desktop-hide"
            style="border: 1px solid #ececec; background-color: #f4f6f8"
          >
            <div class="col-6" style="border-right: 1px solid #ececec">
              <div class="row text-align-center">
                <div style="padding: 10px 10px 0px 10px; margin: auto">
                  <img src="/img/schedule-call-icon.svg" width="10px" />
                </div>
              </div>
              <div class="row">
                <div class="col text-align-center section-text">
                  Schedule a Call
                </div>
              </div>
            </div>
            <div class="col-6" style="border-right: 1px solid #ececec">
              <div class="row text-align-center">
                <div style="padding: 10px 10px 0px 10px; margin: auto">
                  <img src="/img/request-breakout-icon.svg" width="10px" />
                </div>
              </div>
              <div class="row">
                <div class="col text-align-center section-text">
                  Request 1:1 Breakout
                </div>
              </div>
            </div>
          </div>
          <div
            class="row desktop-hide"
            style="border: 1px solid #ececec; background-color: #f4f6f8"
          >
            <div class="col-6" style="border-right: 1px solid #ececec">
              <div class="row text-align-center">
                <div style="padding: 10px 10px 0px 10px; margin: auto">
                  <img src="/img/private-message-icon.svg" width="10px" />
                </div>
              </div>
              <div class="row">
                <div class="col text-align-center section-text">
                  Send a Private Message
                </div>
              </div>
            </div>
            <div
              class="col-6"
              style="border-right: 1px solid #ececec; background-color: #ffffff"
            >
              <div class="row text-align-center">
                <div style="padding: 10px 10px 0px 10px; margin: auto">
                  <svg
                    width="10px"
                    height="10px"
                    viewBox="0 0 22 22"
                    version="1.1"
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                  >
                    <title>muted-icon</title>
                    <g
                      id="muted-icon"
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <path
                        id="Combined-Shape"
                        d="M17.5282275,3.54141657 C17.9088122,3.25232796 18.4480549,3.26498167 18.7965186,3.61344538 C19.1761299,3.99403004 19.1761299,4.61016839 18.7965186,4.9897797 L18.7965186,4.9897797 L13.7204341,10.0658642 L13.7204341,10.7306706 C13.7184874,12.6160735 12.1893352,14.1442523 10.3039324,14.146199 C10.0975796,14.146199 9.89706693,14.1199182 9.70142111,14.0848772 L9.70142111,14.0848772 L8.37472827,15.41157 C8.96750592,15.6656176 9.61965867,15.8077285 10.3039324,15.8077285 C13.0205866,15.8077285 15.2310924,13.5962493 15.2310924,10.8795951 L15.2310924,10.8795951 L15.2310924,10.5554654 C15.2310924,10.0181694 15.6681321,9.58210311 16.2044548,9.58210311 C16.7427241,9.58210311 17.1778171,10.0181694 17.1778171,10.5554654 L17.1778171,10.5554654 L17.1778171,10.8795951 C17.1778171,14.3389248 14.6071672,17.2015833 11.2772947,17.6765841 L11.2772947,17.6765841 L11.2772947,19.0266377 C11.2772947,19.5639337 10.8412284,20 10.3039324,20 C9.76566302,20 9.33057007,19.5639337 9.33057007,19.0266377 L9.33057007,19.0266377 L9.33057007,17.6765841 C8.46719769,17.5539405 7.65541352,17.2736121 6.92539178,16.8599332 L6.92539178,16.8599332 L4.1610428,19.6242821 C3.97123714,19.8150612 3.72205639,19.9094773 3.47287564,19.9094773 C3.22466825,19.9094773 2.97548749,19.8150612 2.78470848,19.6242821 C2.40509717,19.2446708 2.40509717,18.6285325 2.78470848,18.2479478 L2.78470848,18.2479478 L3.07963726,17.9539924 C3.1146783,17.9267383 3.15555952,17.9140846 3.18768048,17.8819636 L3.18768048,17.8819636 Z M4.40185263,9.58200578 C4.94012199,9.58200578 5.37521495,10.0180721 5.37521495,10.5553681 L5.37521495,10.5553681 L5.37521495,10.8794977 C5.37521495,11.4917426 5.49980533,12.0708932 5.70615814,12.6111093 L5.70615814,12.6111093 L4.22762078,14.0886733 C3.71855229,13.1308848 3.42849032,12.0387723 3.42849032,10.8794977 L3.42849032,10.8794977 L3.42849032,10.5553681 C3.42849032,10.0180721 3.86455663,9.58200578 4.40185263,9.58200578 Z M10.303835,2 C11.9381104,2 13.2988709,3.14856754 13.6366276,4.68063982 L13.6366276,4.68063982 L6.95254859,11.3647189 C6.91361409,11.158366 6.88733331,10.9471464 6.88733331,10.7300866 L6.88733331,10.7300866 L6.88733331,5.41650174 C6.88733331,3.5291522 8.41745888,2 10.303835,2 Z"
                        :fill="`${miyColor}`"
                      ></path>
                    </g>
                  </svg>
                </div>
              </div>
              <div class="row">
                <div class="col text-align-center section-text">Mute Sean</div>
              </div>
            </div>
          </div>
          <div
            class="row desktop-hide"
            style="border: 1px solid #ececec; background-color: #f4f6f8"
          >
            <div class="col-6" style="border-right: 1px solid #ececec">
              <div class="row text-align-center">
                <div style="padding: 10px 10px 0px 10px; margin: auto">
                  <img src="/img/contact-details-icon.svg" width="10px" />
                </div>
              </div>
              <div class="row">
                <div class="col text-align-center section-text">
                  Sean's Contact Details
                </div>
              </div>
            </div>
            <div class="col-6" style="border-right: 1px solid #ececec">
              <div class="row text-align-center">
                <div style="padding: 10px 10px 0px 10px; margin: auto">
                  <img src="/img/latency-icon.svg" width="10px" />
                </div>
              </div>
              <div class="row">
                <div class="col text-align-center section-text">
                  Sean's Latency
                </div>
              </div>
            </div>
          </div>
          <div
            class="row"
            style="
              background-color: #ffffff;
              border-radius: 0px 0px 5px 5px;
              padding: 10px 5px 5px 5px;
            "
          >
            <div class="col-3 text-align-center">
              <img
                src="/img/landingPage/facebook-icon.svg"
                class="social-icon"
              />
            </div>
            <div class="col-3 text-align-center">
              <img
                src="/img/landingPage/linkedin-icon.svg"
                class="social-icon"
              />
            </div>
            <div class="col-3 text-align-center">
              <img
                src="/img/landingPage/twitter-icon.svg"
                class="social-icon"
              />
            </div>
            <div class="col-3 text-align-center">
              <img
                src="/img/landingPage/instagram-icon.svg"
                class="social-icon"
              />
            </div>
          </div>
          <div
            class="row mobile-hide"
            style="
              background-color: #ffffff;
              border-radius: 0px 0px 25px 25px;
              padding: 30px 5px;
            "
          >
            <div class="col-3 text-align-center">
              <div
                style="
                  width: 50px;
                  height: 50px;
                  margin: auto;
                  border-radius: 50%;
                  background-color: #8b98a9;
                "
              />
            </div>
            <div class="col-3">
              <div
                :style="`width: 40px; height: 40px; margin: auto; border-radius: 50%; background-color: ${miyColor}`"
              />
            </div>
            <div class="col-3">
              <div
                style="
                  width: 40px;
                  height: 40px;
                  margin: auto;
                  border-radius: 50%;
                  background-color: #8b98a9;
                "
              />
            </div>
            <div class="col-3">
              <div
                style="
                  width: 40px;
                  height: 40px;
                  margin: auto;
                  border-radius: 50%;
                  background-color: #8b98a9;
                "
              />
            </div>
          </div>
          <div class="text-align-center close-meeting">Close</div>
        </div>
      </div>
      <div
        :style="`
          width: 100%;
          background-color: ${miyBackgroundColor2};
          height: 63vw;
          border-radius: 10px;
          min-height: 400px;
        `"
      >
        <div
          :style="`
            width: 40px;
            height: 100px;
            border-radius: 10px;
            background-color: ${miyBackgroundColor1};
          `"
        >
          <div
            :style="`
              width: 52vw;
              height: 52vw;
              background-color: ${miyBackgroundColor1};
              top: -2.05vw;
              float: left;
              border-radius: 50%;
              left: -15vw;
              position: relative;
              clip-path: polygon(36% 4%, 100% 4%, 100% 100%, 36% 100%);
            `"
          ></div>
          <div
            :style="`
              width: 52vw;
              height: 52vw;
              background-color: ${miyBackgroundColor1};
              border-radius: 50%;
              clip-path: polygon(33% 7%, 100% 7%, 100% 100%, 33% 100%);
              margin-top: -54vw;
              float: left;
              left: -17.15vw;
              position: relative;
            `"
          ></div>
        </div>
      </div>
    </div>
    <!--<div class="col-1" />-->
    <div class="col-4 mobile-hide items-center">
      <div
        class="mobile-hide"
        style="margin: 12vw auto 0 auto; max-width: 345px"
      >
        <div
          style="
            font-size: 43px;
            font-weight: bold;
            margin-top: 95px;
            line-height: 56px;
          "
        >
          Make it
          <br />
          Yours.
        </div>
        <div style="font-size: 14pt; margin-top: 27px">
          Currently stuck taking your meetings on unbranded third party apps
          with security issues? Is your brand poorly presented during a pitch?
          <span style="font-weight: bold">
            Your brand powered by Chord Video will move video chat from lame to
            great.
          </span>
        </div>
        <div class="row" style="margin-top: 5vw; height: 50px">
          <div class="col-3">
            <div
              style="
                width: 55px;
                height: 55px;
                background-color: #ffffff;
                border-radius: 50%;
              "
            >
              <div
                style="
                  width: 50%;
                  height: 50%;
                  margin: 25%;
                  border-radius: 50%;
                  background-color: #99c9ff;
                  cursor: pointer;
                "
                @click="switchColor('#99C9FF')"
              />
            </div>
          </div>
          <div class="col-3">
            <div
              class="miy-active"
              style="
                width: 55px;
                height: 55px;
                background-color: #ffffff;
                border-radius: 50%;
              "
            >
              <div
                style="
                  width: 50%;
                  height: 50%;
                  margin: 25%;
                  border-radius: 50%;
                  background-color: #c20112;
                  cursor: pointer;
                "
                @click="switchColor('#C20112')"
              />
            </div>
          </div>
          <div class="col-3">
            <div
              style="
                width: 55px;
                height: 55px;
                background-color: #ffffff;
                border-radius: 50%;
              "
            >
              <div
                style="
                  width: 50%;
                  height: 50%;
                  margin: 25%;
                  border-radius: 50%;
                  background-color: #fac1ad;
                  cursor: pointer;
                "
                @click="switchColor('#FAC1AD')"
              />
            </div>
          </div>
          <div class="col-3"></div>
        </div>
        <div class="row" style="margin-top: 45px">
          <BasicButton
            button-text="Get a Demo"
            use-background
            color="#007FA9"
            :on-click="demoButtonClicked"
          />
          <BasicButton
            button-text="Sign Up"
            color="#007FA9"
            icon="/img/ce-arrow.svg"
            font-color-class="ce-color"
            :on-click="signupButtonClicked"
            rotate-icon
          />
        </div>
        <div class="row" style="margin-top: 15vw; width: 90%">
          <div class="full-width text-align-right">
            <img src="/img/landingPage/powered-by-ce.png" style="width: 85%" />
          </div>
        </div>
      </div>
    </div>
    <div class="desktop-hide col-12">
      <div class="row" style="margin-top: 5vw; height: 50px">
        <div class="col-2"></div>
        <div class="col-3 text-align-center">
          <div
            style="
              width: 55px;
              height: 55px;
              background-color: #ffffff;
              border-radius: 50%;
            "
          >
            <div
              style="
                width: 50%;
                height: 50%;
                margin: 25%;
                border-radius: 50%;
                background-color: #99c9ff;
                cursor: pointer;
              "
              @click="switchColor('#99C9FF')"
            />
          </div>
        </div>
        <div class="col-3 text-align-center">
          <div
            class="miy-active"
            style="
              width: 55px;
              height: 55px;
              background-color: #ffffff;
              border-radius: 50%;
            "
          >
            <div
              style="
                width: 50%;
                height: 50%;
                margin: 25%;
                border-radius: 50%;
                background-color: #c20112;
                cursor: pointer;
              "
              @click="switchColor('#C20112')"
            />
          </div>
        </div>
        <div class="col-3 text-align-center">
          <div
            style="
              width: 55px;
              height: 55px;
              background-color: #ffffff;
              border-radius: 50%;
            "
          >
            <div
              style="
                width: 50%;
                height: 50%;
                margin: 25%;
                border-radius: 50%;
                background-color: #fac1ad;
                cursor: pointer;
              "
              @click="switchColor('#FAC1AD')"
            />
          </div>
        </div>
        <div class="col-1"></div>
      </div>
    </div>
    <SignupModal ref="signupModal" />
  </div>
</template>

<script>
import BasicButton from 'components/landingPage/BasicButton'
import SignupModal from 'components/SignupModal'
export default {
  name: 'PageIndex',
  components: {
    BasicButton,
    SignupModal
  },
  data() {
    return {
      miyColor: '#C20111',
      miyBackgroundColor1: '#F3CCD0',
      miyBackgroundColor2: '#F9E6E7',
      bgColors: {
        '#C20112': ['#F3CCD0', '#F9E6E7'],
        '#FAC1AD': ['#FCE0D6', '#FEF0EA'],
        '#99C9FF': ['#CCE4FF', '#E6F1FF']
      }
    }
  },
  methods: {
    switchColor(color) {
      var coll = document.getElementsByClassName('miy-active')
      while (coll.length > 0) {
        coll[0].setAttribute('class', '')
      }
      event.target.parentNode.setAttribute('class', 'miy-active')
      this.miyColor = color
      this.miyBackgroundColor1 = this.bgColors[color][0]
      this.miyBackgroundColor2 = this.bgColors[color][1]
    },
    signupButtonClicked() {
      this.$refs['signupModal'].showModal = true
    },
    demoButtonClicked() {}
  }
}
</script>

<style lang="scss" scoped>
.miy-active {
  border: 2px solid #005977;
}

.social-icon {
  height: 40px;
  width: 40px;
}

.start-meeting {
  color: #ffffff;
  font-weight: bold;
  padding: 15px;
  font-size: 13pt;
  border-bottom-left-radius: 21px;
  border-bottom-right-radius: 21px;
}

.standup-date {
  font-size: 10pt;
  width: 100%;
  background-color: #f4f6f8;
  border-radius: 0px 0px 20px 20px;
  padding: 25px;
  font-weight: bold;
}

.standup-details {
  width: 100%;
  background-color: #ffffff;
  border-radius: 20px 20px 0px 0px;
  padding: 20px;
  font-weight: bold;
}

.standup-details-outer {
  width: 22.5vw;
  border-radius: 21px;
  margin-top: -25vw;
  margin-left: 12vw;
}

.standup-outer-container {
  width: 14vw;
  margin-top: 17.5vw;
  border-radius: 21px;
}

.standup-outer-container-mobile {
  width: 40%;
  border-radius: 7px;
  font-size: 5pt !important;
}

.standup-outer-container-mobile .start-meeting {
  color: #ffffff;
  font-weight: bold;
  padding: 5px;
  font-size: 7pt;
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
}

.standup-outer-container-mobile .standup-date {
  font-size: 5pt;
  width: 100%;
  background-color: #f4f6f8;
  border-radius: 0px 0px 5px 5px;
  padding: 10px;
  font-weight: bold;
  line-height: 10pt !important;
}

.standup-outer-container-mobile .standup-inner-container {
  border-radius: 5px 5px 0px 0px;
  padding: 10px !important;
}

.big-box .standup-details {
  font-size: 8pt !important;
  padding: 10px;
  border-radius: 5px 5px 0px 0px;
}

.big-box .close-meeting {
  color: #ffffff !important;
  font-weight: bold;
  padding: 10px;
  font-size: 9pt;
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
}

.big-box .section-text {
  padding: 5px 5px 10px 5px;
  color: #8d98a7;
  font-size: 5pt;
}

.big-box .social-icon {
  height: 20px;
  width: 20px;
}

.standup-inner-container {
  width: 100%;
  background-color: #ffffff;
  border-radius: 20px 20px 0px 0px;
  padding: 25px;
  font-weight: bold;
}
</style>
