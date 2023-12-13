<template>
  <div id="main">
    <Navbar/>
    <Hero/>
    <About/>
    <Category/>
    <Bottom/>
    <Foot/>
  </div>
</template>

<script>
import Hero from './components/Hero.vue';
import Navbar from './components/Navbar.vue'
import Category from './components/Category.vue';
import About from './components/About.vue';
import Bottom from './components/bottom.vue'
import Foot from './components/Foot.vue'
export default {
  components: {
    Hero, Navbar, Category, About, Bottom, Foot
  },
}

</script>

<style lang="scss" scoped></style>