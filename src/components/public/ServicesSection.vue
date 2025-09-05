<template>
  <section id="services" class="py-20 bg-blue-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div
        class="text-center mb-16 animate-fade-in-up"
        ref="servicesTitle"
      >
        <h2 class="text-4xl font-bold text-orange-600 mb-6">Service Time</h2>
        <p class="text-lg text-white">Join us for worship and fellowship</p>
      </div>
      
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          class="bg-orange-600 p-8 rounded-lg text-center animate-fade-in-up animation-delay-300"
          ref="serviceCard1"
        >
          <i class="fas fa-sun text-3xl text-blue-600 mb-4"></i>
          <h3 class="text-xl font-semibold text-white mb-2">
            Sunday Morning Service
          </h3>
          <p class="text-gray-900 mb-2">9:30 AM - 12:00 PM</p>
          <p class="text-sm text-gray-900">
            Main worship service with praise, worship, and biblical teaching
          </p>
        </div>
        
        <div
          class="bg-orange-600 p-8 rounded-lg text-center animate-fade-in-up animation-delay-500"
          ref="serviceCard2"
        >
          <i class="fas fa-moon text-3xl text-blue-600 mb-4"></i>
          <h3 class="text-xl font-semibold text-white mb-2">
            Friday Praise & worship
            
          </h3>
          <p class="text-gray-900 mb-2">5:00 PM - 6:00 PM</p>
          <p class="text-sm text-gray-900">
            Evening worship with prayer and communion
          </p>
        </div>
        
        <div
          class="bg-orange-600 p-8 rounded-lg text-center animate-fade-in-up animation-delay-700"
          ref="serviceCard3"
        >
          <i class="fas fa-book-open text-3xl text-blue-600 mb-4"></i>
          <h3 class="text-xl font-semibold text-white
           mb-2">
            Wednesday  Prayers
          </h3>
          <p class="text-gray-900 mb-2">5:30 PM - 6:30 PM</p>
          <p class="text-sm text-gray-900">
           Prayer sessions that bring hearts together in unity
          </p>
        </div>
      </div>
    </div>
    
    <!-- Founder Section -->
    <div class="mt-20">
      <div class="text-center mb-16 animate-fade-in-up" ref="founderTitle">
        <h2 class="text-4xl font-bold text-orange-600 mb-6">Founder</h2>
        <p class="text-lg text-white">Leading with Vision and Faith</p>
      </div>
      
      <div class="flex flex-col md:flex-row items-center gap-12 animate-fade-in-up animation-delay-300" ref="founderContent">
        <div class="md:w-1/2">
          <img
            :src="profileImageUrl"
            alt="Church Founder"
            class="rounded-lg shadow-xl w-full h-[500px] object-cover object-top"
          />
        </div>
        <div class="md:w-1/2 text-left">
          <h3 class="text-2xl font-bold text-orange-600 mb-4">
            Dr. Emily Cheposero Tumwet
          </h3>
          <p class="text-white mb-6 leading-relaxed">
            With a passion for ministry and a heart for God's people, Dr. Emily
            Cheposero Tumwet leads Jesus Christ Solution Ministry Church with
            wisdom, grace, and an unwavering commitment to spreading the Word of
            God. She is a devoted servant of Christ, dedicated to guiding
            believers in their spiritual journey and empowering them to live
            according to God's purpose. Through her powerful teachings,
            heartfelt prayers, and deep biblical insights, she continues to
            transform lives and bring hope to many.
          </p>
          <p class="text-white mb-6 leading-relaxed">
            Her leadership is centered on faith, love, and the power of the Holy
            Spirit to bring healing and restoration to all who seek Christ.
          </p>
          <div class="flex gap-8">
          
            </div>
          </div>
        </div>
      </div>

  </section>
</template>

<script lang="ts" setup>
import { ref, onMounted } from 'vue'

// Template refs
const servicesTitle = ref(null)
const serviceCard1 = ref(null)
const serviceCard2 = ref(null)
const serviceCard3 = ref(null)
const founderTitle = ref(null)
const founderContent = ref(null)

// Founder image

import founderImageUrl from '../../assets/jcsm.jpg'


// Optional: Add intersection observer for scroll-triggered animations
onMounted(() => {
  const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
  }

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('animate-visible')
      }
    })
  }, observerOptions)

  // Observe all animated elements
  const elements = [
    servicesTitle.value,
    serviceCard1.value,
    serviceCard2.value,
    serviceCard3.value,
    founderTitle.value,
    founderContent.value
  ]

  elements.forEach(el => {
    if (el) observer.observe(el)
  })
})
</script>

<style scoped>
/* Animation keyframes */
@keyframes fadeInUp {
  from {
    opacity: 1;
    transform: translateY(30px);
  }
  to {
    opacity:2 ;
    transform: translateY(0);
  }
}

/* Animation classes */
.animate-fade-in-up {
  animation: fadeInUp 2s ease-out forwards;
}

/* Animation delays */
.animation-delay-300 {
  animation-delay: 0.3s;
}

.animation-delay-500 {
  animation-delay: 0.5s;
}

.animation-delay-700 {
  animation-delay: 0.7s;
}

/* Fallback visibility - ensures content is always visible */
.animate-fade-in-up {
  opacity: 1;
  transform: none;
}

/* Card hover effects */
.bg-amber-50:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

/* Icon hover effects */
.fas:hover {
  transform: scale(1.1);
  transition: transform 0.3s ease;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .flex {
    gap: 1rem;
  }
  
  .text-3xl {
    font-size: 1.5rem;
  }
}
</style>