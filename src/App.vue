<template>
  <div>
    <app-navbar :title="brandName" :items="menuItems"/>
    <router-view />
  </div>
</template>

<script>
import AppNavbar from "./components/AppNavbar.vue";

export default {
  name: 'App',

  components: {
    AppNavbar,
  },
  data() {
    return ({
      brandName : "Exchangario",
      menuItems : [
          { text : "Home", link : "/" },
          { text : "About", link : "/about" },
          { text : "Faq", link : "/faq"},
          { text : "Login", link : "/login"},
          { text : "Register", link : "/register"},
      ],
    })
  },
}
</script>

<style lang="scss">
  @import 'assets/styles/variables.scss';
  @import '~bulma/bulma.sass';
  @import 'assets/styles/main.scss';
</style>