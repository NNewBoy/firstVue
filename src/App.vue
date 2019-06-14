<template>
  <div>
    <router-view/>
    <FooterGuider v-show="$route.meta.showFooter"/>
  </div>
</template>

<script>
  import FooterGuider from './components/FooterGuide/FooterGuider'

  export default {
    components: {
      FooterGuider
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .app
    color: read
</style>
