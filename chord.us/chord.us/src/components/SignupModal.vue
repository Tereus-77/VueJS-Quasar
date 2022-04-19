<template>
  <q-dialog v-model="showModal">
    <q-card
      style="
        width: 80%;
        max-width: 1200px;
        height: fit-content;
        color: #ffffff !important;
        background-color: transparent;
        border-radius: 25px;
      "
    >
      <div class="row position-relative" style="border-radius: 25px">
        <img src="/img/landingPage/dot-grid.svg" class="dot-grid-1" />
        <div
          class="col-7"
          style="
            z-index: 2;
            background-color: #ffffff;
            padding: 50px 100px;
            height: fit-content;
            position: relative;
          "
        >
          <div
            style="
              background-color: #f9f1e6;
              border-radius: 50%;
              width: 100%;
              height: 100%;
              position: absolute;
              top: -80%;
              z-index: 0;
              left: 15%;
            "
          ></div>
          <div class="signup-text fs-56 dark-color position-relative">
            Sign Up
          </div>
          <div class="fs-16 signup-sub-text dark-color position-relative">
            Enter your work email to get started with CloudEngage.
          </div>
          <div class="row q-col-gutter-md position-relative">
            <div class="col-6">
              <FormInput
                label="First Name"
                input-prop="firstName"
                placeholder="Joanne"
              />
            </div>
            <div class="col-6">
              <FormInput
                label="Last Name"
                input-prop="lastName"
                placeholder="Smith"
              />
            </div>
          </div>
          <div class="row q-col-gutter-md position-relative">
            <div class="col-6">
              <FormInput
                label="Company"
                input-prop="company"
                placeholder="Microsoft"
              />
            </div>
            <div class="col-6">
              <FormInput
                label="Title"
                input-prop="title"
                placeholder="Software Engineer"
              />
            </div>
          </div>
          <div class="row q-col-gutter-md position-relative">
            <div class="col-6">
              <FormInput
                label="Your Email Address"
                input-prop="emailAddress"
                placeholder="joanne@aol.com"
              />
            </div>
            <div class="col-6">
              <FormInput
                label="Mobile"
                input-prop="mobile"
                placeholder="+1 641 555-5555"
              />
            </div>
          </div>
          <div class="row q-col-gutter-md position-relative">
            <div class="col-12">
              <FormInput
                label="Introduction"
                input-prop="introduction"
                use-text-area
              />
            </div>
          </div>
          <div class="row q-col-gutter-md position-relative">
            <div class="col-12" style="margin-top: 15px">
              <input type="checkbox" class="subscription-agreement-checkbox" />
              <span class="fs-12 dark-color font-circStdBook">
                I agree to the
                <a href="" class="subscription-agreement">
                  CloudEngage Subscription Agreement
                </a>
              </span>
            </div>
          </div>
          <div
            class="row q-col-gutter-md position-relative"
            style="margin-top: 25px"
          >
            <BasicButton
              button-text="Create an Account"
              use-background
              :on-click="accountSignup"
              icon="/img/btn-arrow.svg"
              font-color-class="light-color"
            />
            <BasicButton
              button-text="Cancel"
              :on-click="accountSignupCancel"
              font-color-class="dark-color"
              :remove-icon="false"
            />
          </div>
        </div>
        <div
          class="col-5 position-relative"
          style="background-color: #0a1f44; color: #091f44; z-index: 999"
        >
          <div
            style="
              position: absolute;
              top: 10px;
              right: 20px;
              font-size: 14pt;
              font-weight: bold;
              cursor: pointer;
            "
            @click="hideSignupModal()"
          >
            <span style="margin-right: 10px">Close</span>
            <button type="button" class="close-profile" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div
            style="
              margin-top: 50px;
              padding: 30px;
              z-index: 1;
              position: relative;
            "
          >
            <div class="row q-col-gutter-md">
              <div class="col-1"></div>
              <div class="col-10">
                <img src="/img/welcome-icon.svg" class="welcome-icon" />
              </div>
              <div class="col-1"></div>
            </div>
            <div class="row q-col-gutter-md" style="margin-top: 20px">
              <div class="col-1"></div>
              <div class="col-10">
                <div class="fs-32 light-color font-circStdBold">
                  Welcome Back!
                </div>
                <div class="fs-16 light-color font-circStdBold">
                  Already have an account? Sign in with your email and password.
                </div>
              </div>
              <div class="col-1"></div>
            </div>
            <div class="row q-col-gutter-md">
              <div class="col-1"></div>
              <div class="col-10">
                <FormInput
                  label="Your Email Address"
                  input-prop="loginEmail"
                  :light-theme="false"
                />
                <FormInput
                  label="Password"
                  input-prop="password"
                  :is-password="true"
                  :light-theme="false"
                />
              </div>
              <div class="col-1"></div>
            </div>
            <div class="row q-col-gutter-md">
              <div class="col-1"></div>
              <div class="col-10" style="margin-top: 15px">
                <input type="checkbox" class="stay-signedin-checkbox" />
                <span class="fs-12 light-color font-circStdBook">
                  Keep me signed in.
                </span>
              </div>
              <div class="col-1"></div>
            </div>
            <div class="row q-col-gutter-md" style="margin-top: 20px">
              <div class="col-1"></div>
              <BasicButton
                button-text="Sign In"
                use-border
                :on-click="accountSignin"
              />
              <div class="col-1"></div>
            </div>
          </div>
        </div>
      </div>
    </q-card>
  </q-dialog>
</template>
<script>
import BasicButton from 'components/landingPage/BasicButton'
import FormInput from 'components/FormInput'
export default {
  components: {
    BasicButton,
    FormInput
  },
  props: {},
  data() {
    return {
      showModal: false,
      firstName: '',
      lastName: '',
      companyName: '',
      title: '',
      email: '',
      phone: '',
      introduction: ''
    }
  },
  methods: {
    hideSignupModal() {
      this.showModal = false
    },
    accountSignup() {},
    accountSignin() {},
    accountSignupCancel() {}
  }
}
</script>
<style scoped>
.dot-grid-1 {
  bottom: -35%;
  left: 45%;
  z-index: 9999;
  position: absolute;
}

.signup-text {
  font-family: CircularStdBold;
}

.signup-sub-text {
  font-family: CircularStdBold;
}

.subscription-agreement {
  display: inline-block;
}

.subscription-agreement-checkbox,
.stay-signedin-checkbox {
  display: inline-block;
  height: 20px;
  border-radius: 8px;
  margin-right: 20px;
  vertical-align: bottom;
}

.close-profile {
  cursor: pointer;
}
</style>
