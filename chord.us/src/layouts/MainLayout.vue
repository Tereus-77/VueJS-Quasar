<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container style="overflow-x: hidden">
      <HeaderNav />
      <router-view />
      <Footer />
    </q-page-container>
  </q-layout>
</template>

<script>
import HeaderNav from 'components/HeaderNav.vue'
import Footer from 'components/Footer.vue'

export default {
  name: 'MainLayout',
  components: {
    HeaderNav,
    Footer
  }
}
</script>
