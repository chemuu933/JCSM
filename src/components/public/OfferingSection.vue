<template>
    <section id="offering" class="py-20 bg-blue-100">
<div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
<h2 class="text-4xl font-bold text-amber-800 mb-6 opacity-0 transform translate-y-10 transition-all duration-1000" ref="offeringTitle">Support Our Ministry</h2>
<p class="text-lg text-gray-700 mb-12 leading-relaxed opacity-0 transform translate-y-10 transition-all duration-1000 delay-300" ref="offeringSubtitle">
Your generous giving helps us continue our mission of spreading God's love and serving our community. Every contribution makes a difference in the lives we touch.
</p>
<div class="grid md:grid-cols-2 gap-8 mb-12">
<div class="bg-amber-50 p-8 rounded-lg opacity-0 transform translate-x-[-50px] transition-all duration-1000 delay-500" ref="offeringCard1">
<i class="fas fa-hand-holding-heart text-4xl text-blue-300 mb-4"></i>
<h3 class="text-xl font-semibold text-amber-800 mb-3">Online Giving</h3>
<p class="text-gray-600 mb-4">Make a secure online donation to support our ministry and outreach programs.</p>
<button class="bg-amber-800 hover:bg-amber-700 text-white px-6 py-3 !rounded-button whitespace-nowrap cursor-pointer transition-colors duration-300">
Give Online
</button>
</div>
<div class="bg-amber-50 p-8 rounded-lg opacity-0 transform translate-x-[50px] transition-all duration-1000 delay-700" ref="offeringCard2">
<i class="fas fa-church text-4xl text-blue-300 mb-4"></i>
<h3 class="text-xl font-semibold text-amber-800 mb-3">In-Person Giving</h3>
<p class="text-gray-600 mb-4">You can also give during our worship services or visit our church office.</p>
<button class="bg-amber-800 hover:bg-amber-700 text-white px-6 py-3 !rounded-button whitespace-nowrap cursor-pointer transition-colors duration-300">
Visit Us
</button>
</div>
</div>
<div class="bg-blue-50 p-8 rounded-lg opacity-0 transform translate-y-10 transition-all duration-1000 delay-900" ref="offeringInfo">
<h4 class="text-lg font-semibold text-amber-800 mb-3">Ways Your Giving Helps</h4>
<div class="grid md:grid-cols-3 gap-6 text-sm text-gray-600">
<div>
<i class="fas fa-users text-blue-300 mb-2"></i>
<p>Community outreach programs</p>
</div>
<div>
<i class="fas fa-home text-blue-300 mb-2"></i>
<p>Church facilities and maintenance</p>
</div>
<div>
<i class="fas fa-graduation-cap text-blue-300 mb-2"></i>
<p>Educational and youth programs</p>
</div>
</div>
</div>
</div>
</section>
</template>
<script lang="ts" setup>
const offeringTitle = ref(null);
const offeringSubtitle = ref(null);
const offeringCard1 = ref(null);
const offeringCard2 = ref(null);
const offeringInfo = ref(null);
</script>