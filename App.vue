<template>
  <v-app>
    <router-view name="NavBar"></router-view>
    <router-view name="StudioNavBar"></router-view>
    <v-content
      :class="{
        'content-bg': ![
          'SignIn',
          'SignUp',
          'Dashboard',
          'Video',
          'Detail'
        ].includes(this.$route.name)
          ? true
          : false
      }"
    >
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: 'App'
}
</script>
