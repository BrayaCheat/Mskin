<template>
  <div id="main">
    <Navbar/>
    <Hero/>
    <About/>
    <Category/>
    <Bottom/>
  </div>
</template>

<script>
import Hero from './components/Hero.vue';
import Navbar from './components/Navbar.vue'
import Category from './components/Category.vue';
import About from './components/About.vue';
import Bottom from './components/bottom.vue'
export default {
  components: {
    Hero, Navbar, Category, About, Bottom
  },
}

</script>

<style lang="scss" scoped></style>