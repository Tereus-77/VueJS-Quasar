<template>
  <div id="site-header" style="padding: 0">
    <q-header elevated class="bg-purple">
      <q-bar class="text-align-center gt-sm">
        <div class="chord-logo cursor-pointer col-3 text-align-left">
          <!--<img src="/img/ce-logo.png" class="non-mobile" />-->
          <span class="font-circStdBlack dark-color fs-22">chord</span>
          <span class="inline font-circStdBlack ce-color fs-22">.us</span>
        </div>
        <div class="cursor-pointer col-1 new">Chord Video</div>
        <div class="cursor-pointer menu col-1" @click="menuClicked('products')">
          Products
          <div style="display: inline">
            <div id="products-arrow" class="arrow arrow-down"></div>
          </div>
        </div>
        <div class="cursor-pointer col-1">Customers</div>
        <div class="cursor-pointer col-1">Pricing</div>
        <div class="cursor-pointer menu col-1" @click="menuClicked('company')">
          Company
          <div style="display: inline">
            <div id="company-arrow" class="arrow arrow-down"></div>
          </div>
        </div>
        <div class="cursor-pointer col-1">
          <span
            class="button button-outline fs-11"
            style="padding: 14px 25px; font-size: 11.5pt"
          >
            We're Hiring
          </span>
        </div>
        <div class="cursor-pointer col-3 text-align-right">
          <ProfileDropDown style="margin-right: 70px" />
        </div>
      </q-bar>
      <q-bar class="lt-md" style="padding: 0 20px">
        <div class="cursor-pointer col-6 text-align-left" style="">
          <!--<img src="/img/ce-logo.png" class="mobile-logo" />-->
          <span class="font-circStdBlack dark-color fs-22">chord</span>
          <span class="inline font-circStdBlack ce-color fs-22">.us</span>
        </div>
        <div class="col-6 text-align-right">
          <ProfileDropDown />
        </div>
      </q-bar>
    </q-header>
    <q-expansion-item
      v-model="productsExpanded"
      expand-icon="false"
      :style="`display: ${displayProductsExpansion}`"
    >
      <Products :hide-event="hideMenuNav" />
    </q-expansion-item>
    <q-expansion-item
      v-model="companyExpanded"
      expand-icon="false"
      :style="`display: ${displayCompanyExpansion}`"
    >
      <Company :hide-event="hideMenuNav" />
    </q-expansion-item>
  </div>
</template>

<script>
export default {
  components: {
    Products: () => import('components/navigation/Products'),
    Company: () => import('components/navigation/Company'),
    ProfileDropDown: () => import('components/profile/ProfileDropdown')
  },
  data() {
    return {
      productsExpanded: false,
      companyExpanded: false
    }
  },
  computed: {
    displayProductsExpansion() {
      return this.productsExpanded ? '' : 'none'
    },
    displayCompanyExpansion() {
      return this.companyExpanded ? '' : 'none'
    }
  },
  methods: {
    menuClicked(menu) {
      var expanded = false
      var menuItem = event.target
      var menuActive = document.getElementsByClassName('menu-active')
      switch (menu) {
        case 'products':
          this.productsExpanded = !this.productsExpanded
          this.companyExpanded = false
          expanded = this.productsExpanded
          break
        case 'company':
          this.companyExpanded = !this.companyExpanded
          expanded = this.companyExpanded
          this.productsExpanded = false
          break
        default:
          break
      }
      if (menuActive.length > 0) {
        menuActive[0].classList.remove('menu-active')
        var arrowElement = document.getElementsByClassName('arrow-up')[0]
        arrowElement.classList.remove('arrow-up')
        arrowElement.classList.add('arrow-down')
      }
      if (expanded) {
        menuItem.classList.add('menu-active')
      }
      document
        .getElementById(menu + '-arrow')
        .setAttribute(
          'class',
          menu + '-arrow arrow ' + (expanded ? 'arrow-up' : 'arrow-down')
        )
    },
    hideMenuNav() {
      var menuActive = document.getElementsByClassName('menu-active')
      this.productsExpanded = false
      this.companyExpanded = false
      if (menuActive.length > 0) {
        menuActive[0].classList.remove('menu-active')
        var arrowElement = document.getElementsByClassName('arrow-up')[0]
        arrowElement.classList.remove('arrow-up')
        arrowElement.classList.add('arrow-down')
      }
    }
  }
}
</script>

<style lang="scss">
.menu-active {
  background-color: #f8f0e4;
  border-radius: 25px;
  padding: 12px 0px;
  border: 1px solid #eec69e;
}

.q-item {
  display: none !important;
}

.mobile-logo {
  width: 167px;
  height: 34px;
}

.chord-logo {
  margin-left: 20px !important;
}

.chord-logo span {
  margin-right: 0 !important;
}

#site-header {
  padding: 0 15px;
}

svg {
  font-family: CircularStdBold;
}
</style>
