<template>
<div>
  <Header/>
  <MainTop/>
  <MainMiddle/>
</div>
</template>

<script>
import Header from './Header.vue';
import MainTop from './MainTop.vue';
import MainMiddle  from './MainMiddle.vue';
export default {
  name: "main.vue",
  components: {MainMiddle, Header,MainTop}
}
</script>

<style scoped>

</style>