<template>
    <div>
      <home-hero/>
      <home-list :exchanges="exchanges"/>
      <home-pagination/>    
    </div>
  </template>
  
  <script>
  import HomeHero from "../components/HomeHero.vue";
  import HomeList from "../components/HomeList.vue";
  import HomePagination from "../components/HomePagination.vue";
  
  export default {
    components: {
      HomeList,
      HomeHero,
      HomePagination,
    },
    computed: {
      exchanges() {
        return this.$store.state.exchanges
      }
    },
    created() {
      this.$store.dispatch("getExchanges")
    }
  }
  </script>