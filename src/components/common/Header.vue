<template>
    <nav class="fixed top-0 left-0 right-0 bg-blue-800 shadow-md z-50">
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="flex justify-between items-center h-16">
<!-- Logo -->
<div class="flex-shrink-0 flex items-center gap-3">
<div class="w-10 h-10 bg-white rounded-full flex items-center justify-center">
<i class="fas fa-cross text-blue-600 text-xl"></i>
</div>
<h1 class="text-xl font-bold text-orange-600">JESUS CHRIST SOLUTION MINISTRY</h1>
</div>
<!-- Desktop Navigation -->
<div class="hidden md:block">
<div class="ml-10 flex items-baseline space-x-8">
<a href="#home" class="text-orange-600 hover:text-white px-3 py-2 text-sm font-medium cursor-pointer transition-colors duration-300">Home</a>
<a href="#about" class="text-orange-600 hover:text-white px-3 py-2 text-sm font-medium cursor-pointer transition-colors duration-300">About Us</a>
<a href="#events" class="text-orange-600 hover:text-white px-3 py-2 text-sm font-medium cursor-pointer transition-colors duration-300">Events</a>
<a href="#services" class="text-orange-600 hover:text-white px-3 py-2 text-sm font-medium cursor-pointer transition-colors duration-300">Services</a>
<a href="#offering" class="text-orange-600 hover:text-white px-3 py-2 text-sm font-medium cursor-pointer transition-colors duration-300">Offering</a>
</div>
</div>
<!-- Mobile menu button -->
<div class="md:hidden">
<button @click="mobileMenuOpen = !mobileMenuOpen" class="text-white hover:text-blue-200 cursor-pointer">
<i class="fas fa-bars text-xl"></i>
</button>
</div>
</div>
<!-- Mobile Navigation -->
<div v-if="mobileMenuOpen" class="md:hidden">
<div class="px-2 pt-2 pb-3 space-y-1 sm:px-3 bg-blue-700 border-t border-blue-500">
<a href="#home" class="text-orange-600  hover:text-white  block px-3 py-2 text-base font-medium cursor-pointer">Home</a>
<a href="#about" class="text-orange-600  hover:text-white  block px-3 py-2 text-base font-medium cursor-pointer">About Us</a>
<a href="#events" class="text-orange-600  hover:text-white  block px-3 py-2 text-base font-medium cursor-pointer">Events</a>
<a href="#services" class="text-orange-600  hover:text-white  block px-3 py-2 text-base font-medium cursor-pointer">Services</a>
<a href="#offering" class="text-orange-600 hover:text-white  block px-3 py-2 text-base font-medium cursor-pointer">Offering</a>
</div>
</div>
</div>
</nav>
</template>
<script lang="ts" setup>
import { ref, onMounted } from 'vue';
const mobileMenuOpen = ref(false);
const newsletterEmail = ref('');

</script>
<style scoped>
.\!rounded-button {
border-radius: 0.5rem;
}
html {
scroll-behavior: smooth;
}
body {
font-family: 'Open Sans', sans-serif;
min-height: 1024px;
}
h1, h2, h3, h4, h5, h6 {
font-family: 'Playfair Display', serif;
}
input:focus {
outline: none;
box-shadow: 0 0 0 2px #A7C7E7;
}
input[type="number"]::-webkit-outer-spin-button,
input[type="number"]::-webkit-inner-spin-button {
-webkit-appearance: none;
margin: 0;
}
input[type="number"] {
appearance: textfield;
-moz-appearance: textfield;
}
</style>"