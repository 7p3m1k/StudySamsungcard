<template>
<div>
  <Header/>
  <MainTop/>
  <MainMiddle/>
  <MainBottom/>
  <Footer/>
</div>
</template>

<script>
import Header from './Header.vue';
import MainTop from './MainTop.vue';
import MainMiddle from './MainMiddle.vue';
import Footer from './Footer.vue';
import MainBottom from './MainBottom.vue';
export default {
  name: "main.vue",
  components: {MainBottom, Footer, MainMiddle, Header,MainTop}
}
</script>

<style scoped>

</style>