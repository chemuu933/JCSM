<template>
   <div class="min-h-screen bg-blue-800">
   <Header />
    <HeroSection />
     <AboutSection />
     <ServicesSection />
     <EventSection />
     <Footer />
     </div>
</template>

<script setup>
import Header from "./components/common/Header.vue";
import HeroSection from "./components/public/HeroSection.vue";
import AboutSection from "./components/public/AboutSection.vue";
import ServicesSection from "./components/public/ServicesSection.vue";
//import EventSection from "./components/public/EventSection.vue";
import Footer from "./components/common/Footer.vue";  
</script>



