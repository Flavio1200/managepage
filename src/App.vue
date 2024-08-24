<script setup>
import navbar from './components/navbar.vue'
import hero from './components/hero.vue'
import Info from './components/Info.vue'
import Testimonies from './components/Testimonies.vue'
import Startnow from './components/Startnow.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="cont">
    <navbar/>
    <hero/>
  </div>
  
  <Info/>
  <Testimonies/>
  <Startnow/>
  <Footer/>
</template>

<style scoped>
  .cont{
    background-image: url(/images/bg-simplify-2.svg);
    background-repeat: no-repeat; 
    background-size: cover;
    background-position: center ;
    /* background-color: #000; */
  }
</style>