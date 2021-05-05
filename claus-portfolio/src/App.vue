<template>
  <v-app>
      <Navigation></Navigation>
    <v-main>
      <router-view/>
    </v-main>
     <Footer></Footer>
  </v-app>
</template>

<script>
   import Navigation from "./components/Navigation.vue";
   import Footer from "./components/Footer";

export default {
  name: 'App',


        components: {
            Navigation,
            Footer
        },

  data: () => ({
    //
  }),
};
</script>

<style lang="scss" scoped >

    *{
        margin: 0 !important; ;
        padding: 0 !important ;
    }
    
    .carousel-wrapper{
        filter:brightness(0.7);
    }

    .info_banner{
        position: absolute !important;
        z-index: 99 !important;
        width: 300px;
        height: 300px;
        background-color: green;
    }

    .display-3{
        color: white;
    }



</style>

