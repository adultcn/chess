<template>
  <div id="app">
    <top-header></top-header>
    <router-view/>
    <footer-page></footer-page>
  </div>
</template>

<script type="text/ecmascript-6">
  import TopHeader from '@/components/header'
  import footerPage from '@/components/footer'
  export default {
    components: {
        TopHeader,
        footerPage
    }
  }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  font-size: 12px;
}
</style>
