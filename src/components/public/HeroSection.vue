<template>
  <section
    id="home"
    class="relative h-screen flex items-center justify-center bg-cover bg-center"
    :style="{ backgroundImage: `url('${heroImage}')` }"
  >
    <div class="absolute inset-0 bg-blue-800 bg-opacity-40"></div>
    <div class="relative z-10 text-center text-white px-4 max-w-4xl mx-auto">
      <h1
        class="text-5xl md:text-6xl font-bold mb-6 font-serif opacity-1 transform translate-y-10 transition-all duration-1000 delay-500"
        ref="heroTitle"
      >
        Jesus Christ Solution Ministry
        <p>WELCOME</p>
      </h1>
      <p
        class="text-xl md:text-2xl mb-8 leading-relaxed opacity-0 transform translate-y-10 transition-all duration-1000 delay-700"
        ref="heroSubtitle"
      >
        Come to me, all you who are weary and burdened, and I will give you
        rest. – Matthew 11:28
      </p>
      <button
        class="bg-amber-800 hover:bg-amber-700 text-white px-8 py-4 text-lg font-semibold rounded-lg whitespace-nowrap cursor-pointer transition-colors duration-300 opacity-0 transform translate-y-10 transition-all duration-1000 delay-1000"
        ref="heroButton"
        @click="handleJoinUs"
      >
        Join Us Today
      </button>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref, onMounted } from "vue";

// Template refs
const heroTitle = ref(null);
const heroSubtitle = ref(null);
const heroButton = ref(null);

// Hero image
//const heroImage = 'https://readdy.ai/api/search-image?query=peaceful%20church%20interior%20with%20warm%20sunlight%20streaming%20through%20stained%20glass%20windows%20creating%20a%20serene%20atmosphere%20with%20wooden%20pews%20and%20altar%20in%20soft%20brown%20and%20blue%20tones%20for%20spiritual%20worship&width=1440&height=800&seq=hero001&orientation=landscape'

// Event handler
const handleJoinUs = () => {
  console.log("Join Us Today clicked!");
  // Add your join us functionality here
  // For example: scroll to contact section or open registration form
};

onMounted(() => {
  // Hero section animations
  setTimeout(() => {
    if (heroTitle.value) {
      heroTitle.value.style.opacity = "1";
      heroTitle.value.style.transform = "translateY(0)";
    }
  }, 500);

  setTimeout(() => {
    if (heroSubtitle.value) {
      heroSubtitle.value.style.opacity = "1";
      heroSubtitle.value.style.transform = "translateY(0)";
    }
  }, 700);

  setTimeout(() => {
    if (heroButton.value) {
      heroButton.value.style.opacity = "1";
      heroButton.value.style.transform = "translateY(0)";
    }
  }, 1000);
});
</script>

<style scoped>
/* Fallback visibility in case JavaScript doesn't load */
@media (prefers-reduced-motion: reduce) {
  .opacity-0 {
    opacity: 1 !important;
  }
  .transform {
    transform: none !important;
  }
}

/* Additional hero section styling */
#home {
  background-attachment: fixed;
}

/* Button hover effects */
button:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
}

/* Text shadow for better readability */
h1,
p {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}
</style>
