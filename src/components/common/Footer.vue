<template> 
    <footer class="bg-amber-800 text-white py-12">
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="grid md:grid-cols-3 gap-8">
<!-- Contact Info -->
<div>
<h3 class="text-xl font-semibold mb-4">Contact Us</h3>
<div class="space-y-2 text-sm">
<p><i class="fas fa-map-marker-alt mr-2"></i>Rafiki center (Behind Blessing Mini Supermarket)</p>
<p><i class="fas fa-phone mr-2"></i>0792665651</p>
<p><i class="fas fa-envelope mr-2"></i>info@jcsministry.org</p>
</div>
</div>
<!-- Quick Links -->
<div>
<h3 class="text-xl font-semibold mb-4">Quick Links</h3>
<div class="space-y-2 text-sm">
<a href="#home" class="block hover:text-blue-200 cursor-pointer">Home</a>
<a href="#about" class="block hover:text-blue-200 cursor-pointer">About Us</a>
<a href="#services" class="block hover:text-blue-200 cursor-pointer">Services</a>
<a href="#events" class="block hover:text-blue-200 cursor-pointer">Events</a>
<a href="#offering" class="block hover:text-blue-200 cursor-pointer">Offering</a>
</div>
</div>
<!-- Social Media -->
<div>
<h3 class="text-xl font-semibold mb-4">Follow Us</h3>
<div class="flex space-x-4">
<a href="#" class="text-2xl hover:text-blue-200 cursor-pointer"><i class="fab fa-facebook"></i></a>
<!--<a href="#" class="text-2xl hover:text-blue-200 cursor-pointer"><i class="fab fa-twitter"></i></a>-->
<!--<a href="#" class="text-2xl hover:text-blue-200 cursor-pointer"><i class="fab fa-instagram"></i></a>-->
<a href="#" class="text-2xl hover:text-blue-200 cursor-pointer"><i class="fab fa-youtube"></i></a>
</div>
<!-- Newsletter -->
<div class="mt-6">
<h4 class="font-semibold mb-2">Newsletter</h4>
<div class="flex">
<input
type="email"
placeholder="Your email"
class="flex-1 px-3 py-2 text-gray-800 !rounded-button border-none text-sm"
v-model="newsletterEmail"
>
<button class="bg-blue-300 hover:bg-blue-400 text-amber-800 px-4 py-2 ml-2 !rounded-button whitespace-nowrap cursor-pointer transition-colors duration-300">
Subscribe
</button>
</div>
</div>
</div>
</div>
<div class="border-t border-amber-700 mt-8 pt-8 text-center text-sm">
<p>&copy; 2025 Jesus Christ Solution Ministry. All rights reserved.</p>
</div>
</div>
</footer>
</template>
<script lang="ts" setup>
</script>