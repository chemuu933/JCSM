<template>
  <section
    id="home"
    class="relative h-screen flex items-center justify-center bg-cover bg-center"
    :style="{ backgroundImage: `url('${heroImage}')` }"
  >
    <!-- Enhanced gradient overlay for better readability -->
    <div class="absolute inset-0 bg-gradient-to-b from-blue-900/60 via-blue-800/40 to-blue-900/70"></div>
    
    <!-- Animated background elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute top-20 left-10 w-20 h-20 bg-amber-500/10 rounded-full animate-pulse"></div>
      <div class="absolute top-40 right-20 w-16 h-16 bg-blue-400/10 rounded-full animate-pulse animation-delay-1000"></div>
      <div class="absolute bottom-32 left-1/4 w-24 h-24 bg-amber-600/10 rounded-full animate-pulse animation-delay-2000"></div>
    </div>

    <!-- Main content with enhanced styling -->
    <div class="relative z-10 text-center text-white px-4 max-w-5xl mx-auto">

      <!-- Enhanced title with gradient text -->
      <h1
        class="pt-20 text-5xl md:text-7xl font-bold mb-8 font-serif bg-gradient-to-r from-white via-amber-200 to-white bg-clip-text text-transparent opacity-0 transform translate-y-10 transition-all duration-1000 delay-500"
        ref="heroTitle"
      >
        Jesus Christ Solution Ministry
      </h1>

      <!-- Decorative divider -->
      <div 
        class="w-32 h-1 bg-gradient-to-r from-transparent via-amber-400 to-transparent mx-auto mb-8 opacity-0 transform scale-x-0 transition-all duration-1000 delay-600"
        ref="heroDivider"
      ></div>

      <!-- Enhanced subtitle with backdrop -->
      <div 
        class="bg-white/5 backdrop-blur-sm border border-white/10 rounded-2xl p-8 mb-10 opacity-0 transform translate-y-10 transition-all duration-1000 delay-700"
        ref="heroSubtitle"
      >
        <p class="text-xl md:text-2xl leading-relaxed font-light italic">
          "Come to me, all you who are weary and burdened, and I will give you rest."
        </p>
        <p class="text-lg md:text-xl mt-4 text-amber-300 font-medium">
          — Matthew 11:28
        </p>
      </div>

      <!-- Enhanced CTA buttons -->
      <div 
        class="flex flex-col sm:flex-row gap-4 justify-center items-center opacity-0 transform translate-y-10 transition-all duration-1000 delay-1000"
        ref="heroButtons"
      >
        <button
          class="group bg-gradient-to-r from-amber-900 to-amber-700 hover:from-amber-800 hover:to-amber-600 text-white px-10 py-4 text-lg font-semibold rounded-full whitespace-nowrap cursor-pointer transition-all duration-300 transform hover:scale-105 hover:shadow-2xl border-2 border-amber-600/30"
          @click="handleJoinUs"
        >
          <i class="fas fa-hands-praying mr-2 group-hover:animate-pulse"></i>
          Join Us Today
        </button>
        
        <button
          class="group bg-white/10 backdrop-blur-sm hover:bg-white/20 text-white border-2 border-white/30 hover:border-white/50 px-10 py-4 text-lg font-semibold rounded-full whitespace-nowrap cursor-pointer transition-all duration-300 transform hover:scale-105"
          @click="handleLearnMore"
        >
          <i class="fas fa-book-open mr-2 group-hover:animate-pulse"></i>
          Learn More
        </button>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref, onMounted } from "vue";

// Template refs
const heroIcon = ref(null);
const heroTitle = ref(null);
const heroDivider = ref(null);
const heroSubtitle = ref(null);
const heroButtons = ref(null);
const scrollIndicator = ref(null);

// Church hero image - beautiful church interior or exterior
const heroImage = 'https://images.unsplash.com/photo-1520637836862-4d197d17c99a?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80';

// Event handlers
const handleJoinUs = () => {
  console.log("Join Us Today clicked!");
  // Smooth scroll to services section
  document.getElementById('services')?.scrollIntoView({ behavior: 'smooth' });
};

const handleLearnMore = () => {
  console.log("Learn More clicked!");
  // Scroll to about section or open modal
  document.getElementById('about')?.scrollIntoView({ behavior: 'smooth' });
};

onMounted(() => {
  const elements = [
    { ref: heroIcon, delay: 300 },
    { ref: heroTitle, delay: 500 },
    { ref: heroDivider, delay: 600 },
    { ref: heroSubtitle, delay: 700 },
    { ref: heroButtons, delay: 1000 },
    { ref: scrollIndicator, delay: 1200 }
  ];

  elements.forEach(({ ref: elementRef, delay }) => {
    setTimeout(() => {
      if (elementRef.value) {
        elementRef.value.style.opacity = "1";
        elementRef.value.style.transform = elementRef === heroDivider ? "scaleX(1)" : "translateY(0) scale(1)";
      }
    }, delay);
  });
});
</script>

<style scoped>
/* Animation delays */
.animation-delay-1000 {
  animation-delay: 1s;
}

.animation-delay-2000 {
  animation-delay: 2s;
}

/* Fallback visibility for reduced motion */
@media (prefers-reduced-motion: reduce) {
  .opacity-0 {
    opacity: 1 !important;
  }
  .transform {
    transform: none !important;
  }
  .animate-pulse,
  .animate-bounce {
    animation: none !important;
  }
}

/* Enhanced background attachment */
#home {
  background-attachment: fixed;
  position: relative;
}

/* Gradient text support */
.bg-clip-text {
  -webkit-background-clip: text;
  background-clip: text;
}

/* Enhanced button hover effects */
button:hover {
  transform: translateY(-2px) scale(1.05);
}

.group:hover i {
  transform: scale(1.1);
  transition: transform 0.3s ease;
}

/* Text shadow for better readability */
h1, p {
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.5);
}

/* Backdrop blur support */
.backdrop-blur-sm {
  backdrop-filter: blur(4px);
}

/* Custom scrollbar for the page */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #1e40af;
}

::-webkit-scrollbar-thumb {
  background: #d97706;
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: #b45309;
}

/* Enhanced responsive design */
@media (max-width: 768px) {
  h1 {
    font-size: 2.5rem;
  }
  
  .text-xl {
    font-size: 1.125rem;
  }
  
  .px-10 {
    padding-left: 2rem;
    padding-right: 2rem;
  }
}

@media (max-width: 480px) {
  h1 {
    font-size: 2rem;
  }
  
  .px-10 {
    padding-left: 1.5rem;
    padding-right: 1.5rem;
  }
  
  .py-4 {
    padding-top: 0.75rem;
    padding-bottom: 0.75rem;
  }
}
</style>