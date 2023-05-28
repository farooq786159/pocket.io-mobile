<script setup>
import Nav from "../components/menu/Nav.vue"
import homeLanding from "../components/Home/homeLanding.vue";
import homeSecond from "../components/Home/homeSecond.vue";
import homeThird from "../components/Home/homeThird.vue";
import homeForth from "../components/Home/homeForth.vue";
import Footer from "../components/menu/footer.vue"
</script>

<template>
  <main class=" sm:text-center">
      <Nav/>
      
      <homeLanding/>
      <homeSecond/>
      <homeThird/>
      <homeForth/>
      <Footer/>
  </main>
  
</template>

