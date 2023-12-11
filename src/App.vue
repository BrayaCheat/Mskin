<template>
  <div id="main">
    <Navbar/>
    <Hero/>
    <About/>
    <Category/>
  </div>
</template>

<script>
import Hero from './components/Hero.vue';
import Navbar from './components/Navbar.vue'
import Category from './components/Category.vue';
import About from './components/About.vue';
export default {
  components: {
    Hero, Navbar, Category, About
  },
}

</script>

<style lang="scss" scoped></style>