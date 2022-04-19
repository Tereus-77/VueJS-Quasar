<template>
  <div class="q-pa-md">
    <q-btn-dropdown
      rounded
      icon="img:/img/default-profile-image.png"
      :label="firstName"
      style="
        height: 45px;
        background-color: #e0b083 !important;
        min-width: 137px;
      "
    >
      <q-list>
        <q-btn
          flat
          text-color="black"
          label="Profile"
          style="width: 100%; padding: 5px"
          @click="viewProfile = true"
        />
        <q-btn
          flat
          text-color="black"
          label="TF Standard"
          style="width: 100%; padding: 5px"
          @click="embedStandardTypeform"
        />
        <div>
          <a
            class="typeform-share button"
            href="https://form.typeform.com/to/frLRcpVE"
            data-mode="popup"
            target="myIframe"
            style="
              display: inline-block;
              text-decoration: none;
              color: black;
              cursor: pointer;
              font-family: Helvetica, Arial, sans-serif;
              font-size: 12px;
              line-height: 50px;
              text-align: center;
              margin: 0;
              height: 50px;
              padding: 5px;
              width: 100%;
              white-space: nowrap;
              -webkit-font-smoothing: antialiased;
              -moz-osx-font-smoothing: grayscale;
            "
            @click="viewProfileTypeformIframe = true"
            >TF IFRAME
          </a>
        </div>
      </q-list>
    </q-btn-dropdown>
    <q-dialog v-model="viewProfileTypeformStandard">
      <q-card
        style="
          width: 100%;
          max-width: 65%;
          color: #ffffff !important;
          background-color: transparent;
          border-radius: 25px;
        "
      >
        <div class="row" style="border-radius: 25px">
          <div class="col-4" style="background-color: #091f44; z-index: 2">
            <div style="padding: 15% 0% 0% 15%; font-size: 50pt">👋</div>
            <div style="padding: 5% 0% 0% 15%; font-size: 27pt">
              Hi {{ firstName }},
            </div>
            <div style="padding: 5% 23% 5% 15%; font-size: 12pt">
              View and edit any of your accounts below.
            </div>
            <div style="padding: 5% 0% 0% 15%">
              <div class="profile-persona active" @click="switchPersona">
                Personal<img
                  data-v-6afadc37=""
                  src="/img/btn-arrow.svg"
                  class="inline-img"
                  style="float: right; margin: 5px 20px"
                />
              </div>
            </div>
            <div style="padding: 5% 0% 0% 15%">
              <div class="profile-persona" @click="switchPersona">
                Work<img
                  data-v-6afadc37=""
                  src="/img/btn-arrow.svg"
                  class="inline-img"
                  style="float: right; margin: 5px 20px"
                />
              </div>
            </div>
            <div style="padding: 5% 0% 0% 15%">
              <div class="profile-persona" @click="switchPersona">
                Custom<img
                  data-v-6afadc37=""
                  src="/img/btn-arrow.svg"
                  class="inline-img"
                  style="float: right; margin: 5px 20px"
                />
              </div>
            </div>
            <div
              style="
                margin-top: 25%;
                border-top: 1px solid #007fa8;
                padding: 10%;
                text-align: center;
                font-weight: bold;
                text-decoration: underline;
              "
            >
              Settings
            </div>
          </div>
          <div class="col-8" style="background-color: #ffffff">
            <div
              style="
                background-color: #f9f1e6;
                border-radius: 50%;
                width: 900px;
                height: 900px;
                position: absolute;
                top: -96%;
                z-index: 0;
                left: 5%;
              "
            ></div>
            <div
              style="
                position: absolute;
                top: 10px;
                right: 20px;
                font-size: 14pt;
                font-weight: bold;
                cursor: pointer;
              "
              @click="hideProfileModal('TypeformStandard')"
            >
              <span style="margin-right: 10px">Close</span>
              <button type="button" class="close-profile" aria-label="Close">
                <span aria-hidden="true">&times;</span>
              </button>
            </div>
            <div
              id="typeform-standard-container"
              class="typeform-widget"
              data-url="https://form.typeform.com/to/frLRcpVE"
              data-transparency="50"
              style="margin-top: 200px; height: calc(90% - 200px)"
            ></div>
            <div style="color: black">This is the standard typeform embed</div>
          </div>
        </div>
      </q-card>
    </q-dialog>
    <q-dialog v-model="viewProfileTypeformIframe">
      <q-card
        style="
          width: 100%;
          max-width: 65%;
          color: #ffffff !important;
          background-color: transparent;
          border-radius: 25px;
        "
      >
        <div class="row" style="border-radius: 25px">
          <div class="col-4" style="background-color: #091f44; z-index: 2">
            <div style="padding: 15% 0% 0% 15%; font-size: 50pt">👋</div>
            <div style="padding: 5% 0% 0% 15%; font-size: 27pt">
              Hi {{ firstName }},
            </div>
            <div style="padding: 5% 23% 5% 15%; font-size: 12pt">
              View and edit any of your accounts below.
            </div>
            <div style="padding: 5% 0% 0% 15%">
              <div class="profile-persona active" @click="switchPersona">
                Personal<img
                  data-v-6afadc37=""
                  src="/img/btn-arrow.svg"
                  class="inline-img"
                  style="float: right; margin: 5px 20px"
                />
              </div>
            </div>
            <div style="padding: 5% 0% 0% 15%">
              <div class="profile-persona" @click="switchPersona">
                Work<img
                  data-v-6afadc37=""
                  src="/img/btn-arrow.svg"
                  class="inline-img"
                  style="float: right; margin: 5px 20px"
                />
              </div>
            </div>
            <div style="padding: 5% 0% 0% 15%">
              <div class="profile-persona" @click="switchPersona">
                Custom<img
                  data-v-6afadc37=""
                  src="/img/btn-arrow.svg"
                  class="inline-img"
                  style="float: right; margin: 5px 20px"
                />
              </div>
            </div>
            <div
              style="
                margin-top: 25%;
                border-top: 1px solid #007fa8;
                padding: 10%;
                text-align: center;
                font-weight: bold;
                text-decoration: underline;
              "
            >
              Settings
            </div>
          </div>
          <div class="col-8" style="background-color: #ffffff">
            <div
              style="
                background-color: #f9f1e6;
                border-radius: 50%;
                width: 900px;
                height: 900px;
                position: absolute;
                top: -96%;
                z-index: 0;
                left: 5%;
              "
            ></div>
            <div
              style="
                position: absolute;
                top: 10px;
                right: 20px;
                font-size: 14pt;
                font-weight: bold;
                cursor: pointer;
              "
              @click="hideProfileModal('TypeformIframe')"
            >
              <span style="margin-right: 10px">Close</span>
              <button type="button" class="close-profile" aria-label="Close">
                <span aria-hidden="true">&times;</span>
              </button>
            </div>
            <iframe
              name="myIframe"
              height="300px"
              width="100%"
              style="margin-top: 200px; height: calc(90% - 200px)"
            ></iframe>
            <div style="color: black">
              This is the pop-up style contained in an iframe
            </div>
          </div>
        </div>
      </q-card>
    </q-dialog>
    <q-dialog v-model="viewProfile">
      <q-card
        style="
          width: 100%;
          max-width: 65%;
          color: #ffffff !important;
          background-color: transparent;
          border-radius: 25px;
        "
      >
        <div class="row" style="border-radius: 25px">
          <div class="col-4" style="background-color: #091f44; z-index: 2">
            <div style="padding: 15% 0% 0% 15%; font-size: 50pt">👋</div>
            <div style="padding: 5% 0% 0% 15%; font-size: 27pt">
              Hi {{ firstName }},
            </div>
            <div style="padding: 5% 23% 5% 15%; font-size: 12pt">
              View and edit any of your accounts below.
            </div>
            <div style="padding: 5% 0% 0% 15%">
              <div class="profile-persona active" @click="switchPersona">
                Personal<img
                  data-v-6afadc37=""
                  src="/img/btn-arrow.svg"
                  class="inline-img"
                  style="float: right; margin: 5px 20px"
                />
              </div>
            </div>
            <div style="padding: 5% 0% 0% 15%">
              <div class="profile-persona" @click="switchPersona">
                Work<img
                  data-v-6afadc37=""
                  src="/img/btn-arrow.svg"
                  class="inline-img"
                  style="float: right; margin: 5px 20px"
                />
              </div>
            </div>
            <div style="padding: 5% 0% 0% 15%">
              <div class="profile-persona" @click="switchPersona">
                Custom<img
                  data-v-6afadc37=""
                  src="/img/btn-arrow.svg"
                  class="inline-img"
                  style="float: right; margin: 5px 20px"
                />
              </div>
            </div>
            <div
              style="
                margin-top: 25%;
                border-top: 1px solid #007fa8;
                padding: 10%;
                text-align: center;
                font-weight: bold;
                text-decoration: underline;
              "
            >
              Settings
            </div>
          </div>
          <div class="col-8" style="background-color: #ffffff; color: #091f44">
            <div
              style="
                background-color: #f9f1e6;
                border-radius: 50%;
                width: 900px;
                height: 900px;
                position: absolute;
                top: -96%;
                z-index: 0;
                left: 5%;
              "
            ></div>
            <div
              style="
                position: absolute;
                top: 10px;
                right: 20px;
                font-size: 14pt;
                font-weight: bold;
                cursor: pointer;
              "
              @click="hideProfileModal()"
            >
              <span style="margin-right: 10px">Close</span>
              <button type="button" class="close-profile" aria-label="Close">
                <span aria-hidden="true">&times;</span>
              </button>
            </div>
            <div
              style="
                margin-top: 50px;
                padding: 30px 20%;
                z-index: 1;
                position: relative;
              "
            >
              <div class="row">
                <div class="col-3">
                  <img
                    src="/img/default-profile-image.png"
                    style="
                      width: 100px;
                      max-width: 100px;
                      border-radius: 15px;
                      border: 1px solid #979797;
                    "
                  />
                </div>
                <div class="col-9">
                  <div style="font-size: 23pt; font-weight: bold; margin: 5px">
                    {{ firstName }} {{ lastName }}
                  </div>
                  <div style="font-weight: bold; margin: 5px">Spokane, WA</div>
                </div>
              </div>
              <div class="row" style="margin-top: 20px">
                <div class="col-6">
                  <q-input
                    v-model="firstName"
                    :readonly="isEditable"
                    :outlined="!isEditable"
                    borderless
                    label="First Name"
                    style="font-size: 13pt; margin-right: 5px"
                  />
                </div>
                <div class="col-6">
                  <q-input
                    v-model="lastName"
                    :readonly="isEditable"
                    :outlined="!isEditable"
                    borderless
                    label="Last Name"
                    style="font-size: 13pt"
                  />
                </div>
              </div>
              <div class="row" style="margin-top: 20px">
                <div class="col-6">
                  <q-input
                    v-model="emailAddress"
                    :readonly="isEditable"
                    :outlined="!isEditable"
                    borderless
                    label="Email Address"
                    style="font-size: 13pt; margin-right: 5px"
                  />
                </div>
                <div class="col-6">
                  <q-input
                    v-model="phoneNumber"
                    :readonly="isEditable"
                    :outlined="!isEditable"
                    borderless
                    label="Phone Number"
                    style="font-size: 13pt"
                  />
                </div>
              </div>
              <div class="row" style="margin-top: 20px">
                <div class="col-6">
                  <q-input
                    v-model="companyName"
                    :readonly="isEditable"
                    :outlined="!isEditable"
                    borderless
                    label="Company"
                    style="font-size: 13pt; margin-right: 5px"
                  />
                </div>
              </div>
              <div
                class="row"
                style="
                  padding: 40px 0px;
                  border-top: 1px solid #ebebeb;
                  border-bottom: 1px solid #ebebeb;
                  margin-top: 20px;
                "
              >
                <div class="col-4" style="padding-top: 10px; font-weight: bold">
                  Social
                </div>
                <div class="col-2">
                  <div class="social-media justify-center items-center">
                    <img
                      src="/img/landingPage/twitter-icon.png"
                      class="twitter"
                    />
                  </div>
                </div>
                <div class="col-2 justify-center items-center">
                  <div class="social-media">
                    <img
                      src="/img/landingPage/linked-in-icon.png"
                      class="linked-in"
                    />
                  </div>
                </div>
                <div class="col-2 justify-center items-center">
                  <div class="social-media">
                    <img
                      src="/img/landingPage/instagram-icon.png"
                      class="instagram"
                    />
                  </div>
                </div>
                <div class="col-2 justify-center items-center">
                  <div class="social-media">
                    <img
                      src="/img/landingPage/facebook-icon.png"
                      class="facebook"
                    />
                  </div>
                </div>
              </div>
              <div v-if="editable" class="row" style="padding: 40px 0px">
                <div class="col-6">
                  <q-btn
                    no-caps
                    unelevated
                    rounded
                    style="
                      width: 100%;
                      border: 1px solid #bac0c0;
                      background-color: #007fa8;
                      color: white;
                      height: 50px;
                    "
                    label="Share Profile"
                  />
                </div>
                <div class="col-6">
                  <div
                    style="
                      width: 100%;
                      height: 50px;
                      text-decoration: underline;
                      text-align: center;
                      padding-top: 15px;
                      cursor: pointer;
                    "
                    @click="makeEditable"
                  >
                    Edit Profile
                  </div>
                </div>
              </div>
              <div v-else class="row" style="padding: 40px 0px">
                <div class="col-6">
                  <q-btn
                    no-caps
                    unelevated
                    rounded
                    style="
                      width: 100%;
                      border: 1px solid #bac0c0;
                      background-color: #007fa8;
                      color: white;
                      height: 50px;
                    "
                    label="Save Changes"
                    @click="makeEditable(true)"
                  />
                </div>
                <div class="col-6">
                  <div
                    style="
                      width: 100%;
                      height: 50px;
                      text-decoration: underline;
                      text-align: center;
                      padding-top: 15px;
                      cursor: pointer;
                    "
                    @click="makeEditable(false)"
                  >
                    Cancel
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </q-card>
    </q-dialog>
  </div>
</template>
<script>
export default {
  components: {},
  props: {},
  data() {
    return {
      editable: true,
      firstName: 'Sami',
      lastName: 'Jones',
      emailAddress: 'sami@personal.com',
      phoneNumber: '+1 641 355-5555',
      companyName: 'CloudEngage Inc.',
      viewProfile: false,
      viewProfileTypeformIframe: false,
      viewProfileTypeformStandard: false,
      userInfo: {
        firstName: 'Sami',
        lastName: 'Personal',
        emailAddress: 'sami@personal.com',
        phoneNumber: '+1 641 355-5555',
        companyName: 'CloudEngage Inc.'
      },
      details: {}
    }
  },
  computed: {
    profileImageSource() {
      return '/img/default-profile-image.png'
    },
    isEditable() {
      return this.editable
    }
  },
  methods: {
    hideProfileModal(a) {
      this['viewProfile' + (a || '')] = false
    },
    switchPersona() {
      var activePersona = document.getElementsByClassName('profile-persona')
      for (var i = 0; i < activePersona.length; i++) {
        activePersona[i].classList.remove('active')
      }
      event.target.classList.add('active')
    },
    makeEditable(save) {
      if (save) {
        this.userInfo.firstName = this.firstName
        this.userInfo.lastName = this.lastName
        this.userInfo.emailAddress = this.emailAddress
        this.userInfo.phoneNumber = this.phoneNumber
        this.userInfo.companyName = this.companyName
      } else {
        this.firstName = this.userInfo.firstName
        this.lastName = this.userInfo.lastName
        this.emailAddress = this.userInfo.emailAddress
        this.phoneNumber = this.userInfo.phoneNumber
        this.companyName = this.userInfo.companyName
      }
      this.editable = !this.editable
    },
    embedStandardTypeform() {
      this.viewProfileTypeformStandard = true
      if (window.typeformEmbed) {
        var el = document.getElementById('typeform-standard-container')

        try {
          window.typeformEmbed.makeWidget(el, el.getAttribute('data-url'), {
            hideFooter: true,
            hideHeaders: true,
            opacity: 0
          })
        } catch (e) {
          setTimeout(this.embedStandardTypeform, 100)
        }
      }
    }
  }
}
</script>

<style>
button .q-btn__content img.q-icon {
  width: 35px;
  height: 35px;
  border-radius: 50%;
  margin-left: -10px;
}
button.close-profile {
  border: 0;
  background-color: transparent;
  font-size: 20pt;
  color: #0280a9;
  -webkit-user-select: none; /* Chrome/Safari */
  -moz-user-select: none; /* Firefox */
  -ms-user-select: none; /* IE10+ */

  /* Rules below not implemented in browsers yet */
  -o-user-select: none;
  user-select: none;
}
.profile-persona {
  cursor: pointer;
  text-indent: 40px;
  font-size: 15pt;
  padding: 10px;
  border-radius: 25px 0% 0% 25px;
}
.profile-persona:hover {
  background-color: #007fa8;
}
.profile-persona.active {
  background-color: #007fa8;
}
.profile-persona img {
  display: none !important;
}
.profile-persona.active img {
  display: inline !important;
}
.q-dialog div.q-field__label {
  color: #091f44;
}
.social-media {
  height: 36px;
  width: 36px;
  border-radius: 18px;
  border: 1px solid var(--dark-color);
  padding: 5px;
}

.twitter {
  width: 16px;
  height: 13px;
  margin: 6px 4px;
}

.linked-in {
  width: 15px;
  height: 15px;
  margin: 4px 5px;
}

.facebook {
  width: 8px;
  height: 16px;
  margin: 4px 8px;
}

.instagram {
  width: 18px;
  height: 18px;
  margin: 3px;
}
</style>
<style></style>
