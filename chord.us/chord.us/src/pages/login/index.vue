<template>
  <q-page class="flex flex-center" style="overflow-x: hidden">login</q-page>
</template>

<script>
export default {
  name: 'Login',
  async mounted() {
    let users = await this.$axios.$get('/users')
    alert('the number of users in the system ' + users.length)
  }
}
</script>
