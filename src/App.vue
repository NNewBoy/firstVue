<template>
  <div>
    <router-view/>
    <FooterGuider v-show="$route.meta.showFooter"/>
  </div>
</template>

<script>
  import {mapActions} from 'vuex'
  import FooterGuider from './components/FooterGuide/FooterGuider'
  import {reqFoodCategorys} from "./api";

  export default {

    mounted(){
      //this.$store.dispatch('getAddress')
      this.getAddress()
      this.getUserInfo()
    },

    methods:{
      ...mapActions(['getAddress','getUserInfo'])
    },
    components: {
      FooterGuider
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .app
    color: read
</style>
