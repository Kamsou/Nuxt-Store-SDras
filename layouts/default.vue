<template>
  <div>
    <AppNav />
    <nuxt />
  </div>
</template>

<script>
import AppNav from '@/components/AppNav.vue'

export default {
  components: {
    AppNav
  },
}
</script>

<style>
html {
  font-family: 'Montserrat', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background: white;
  color: black;
}

h1, h2, h3 {
  font-family: 'Montserrat', -apple-system, BlinkMacSystemFont, 'Segoe UI',
  Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-weight: normal;
}

h1 {
  font-weight: 45px;
}

a, a:visited, a:active {
  color: #000000;
  text-decoration: none;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}


</style>
