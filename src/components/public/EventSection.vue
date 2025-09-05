<template>
  <section id="events" class="py-20 bg-blue-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16 animate-fade-in-up" ref="eventsTitle">
        <h2 class="text-4xl font-bold text-amber-800 mb-6">Upcoming Events</h2>
        <p class="text-lg text-white">Stay connected with our church community</p>
      </div>
      
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div class="bg-amber-50 rounded-lg shadow-md overflow-hidden animate-slide-in-left animation-delay-300" ref="eventCard1">
          <img :src="eventImage1" alt="Youth Conference" class="w-full h-48 object-cover object-top">
          <div class="p-6">
            <div class="text-blue-600 text-sm font-semibold mb-2">March 15, 2025</div>
            <h3 class="text-xl font-semibold text-amber-800 mb-3">Youth Conference 2025</h3>
            <p class="text-gray-600 mb-4">A special gathering for young people to grow in faith and fellowship with inspiring speakers and worship.</p>
            <button 
              class="bg-amber-800 hover:bg-amber-700 text-white px-4 py-2 rounded-lg whitespace-nowrap cursor-pointer transition-colors duration-300"
              @click="handleLearnMore('youth-conference')"
            >
              Learn More
            </button>
          </div>
        </div>
        
        <div class="bg-amber-50 rounded-lg shadow-md overflow-hidden animate-fade-in-up animation-delay-500" ref="eventCard2">
          <img :src="eventImage2" alt="Community Outreach" class="w-full h-48 object-cover object-top">
          <div class="p-6">
            <div class="text-blue-600 text-sm font-semibold mb-2">March 22, 2025</div>
            <h3 class="text-xl font-semibold text-amber-800 mb-3">Community Outreach Day</h3>
            <p class="text-gray-600 mb-4">Join us as we serve our community through food distribution, free health checkups, and prayer support.</p>
            <button 
              class="bg-amber-800 hover:bg-amber-700 text-white px-4 py-2 rounded-lg whitespace-nowrap cursor-pointer transition-colors duration-300"
              @click="handleVolunteer('community-outreach')"
            >
              Volunteer
            </button>
          </div>
        </div>
        
        <div class="bg-amber-50 rounded-lg shadow-md overflow-hidden animate-slide-in-right animation-delay-700" ref="eventCard3">
          <img :src="eventImage3" alt="Easter Celebration" class="w-full h-48 object-cover object-top">
          <div class="p-6">
            <div class="text-blue-600 text-sm font-semibold mb-2">April 13, 2025</div>
            <h3 class="text-xl font-semibold text-amber-800 mb-3">Easter Celebration</h3>
            <p class="text-gray-600 mb-4">Celebrate the resurrection of Jesus Christ with special worship services, music, and fellowship.</p>
            <button 
              class="bg-amber-800 hover:bg-amber-700 text-white px-4 py-2 rounded-lg whitespace-nowrap cursor-pointer transition-colors duration-300"
              @click="handleJoinUs('easter-celebration')"
            >
              Join Us
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref, onMounted } from 'vue'

// Template refs
const eventsTitle = ref(null)
const eventCard1 = ref(null)
const eventCard2 = ref(null)
const eventCard3 = ref(null)

// Event images
const eventImage1 = 'https://readdy.ai/api/search-image?query=young%20people%20gathering%20in%20modern%20church%20setting%20with%20warm%20lighting%20and%20contemporary%20worship%20atmosphere%20featuring%20brown%20and%20blue%20color%20scheme%20for%20youth%20conference%20event&width=400&height=300&seq=event001&orientation=landscape'
const eventImage2 = 'https://readdy.ai/api/search-image?query=community%20volunteers%20serving%20food%20and%20helping%20people%20in%20outdoor%20setting%20with%20warm%20brown%20and%20soft%20blue%20tones%20showing%20church%20outreach%20and%20charity%20work%20in%20action&width=400&height=300&seq=event002&orientation=landscape'
const eventImage3 = 'https://readdy.ai/api/search-image?query=beautiful%20easter%20celebration%20setup%20with%20cross%20flowers%20and%20warm%20lighting%20in%20church%20sanctuary%20featuring%20brown%20and%20blue%20color%20palette%20for%20resurrection%20sunday%20worship%20service&width=400&height=300&seq=event003&orientation=landscape'

// Event handlers
const handleLearnMore = (eventType: string) => {
  console.log(`Learn more about: ${eventType}`)
  // Add your navigation or modal logic here
}

const handleVolunteer = (eventType: string) => {
  console.log(`Volunteer for: ${eventType}`)
  // Add your volunteer registration logic here
}

const handleJoinUs = (eventType: string) => {
  console.log(`Join us for: ${eventType}`)
  // Add your event registration logic here
}

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
    eventsTitle.value,
    eventCard1.value,
    eventCard2.value,
    eventCard3.value
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
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  from {
    opacity: 0;
    transform: translateX(50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

/* Animation classes */
.animate-fade-in-up {
  animation: fadeInUp 1s ease-out forwards;
}

.animate-slide-in-left {
  animation: slideInLeft 1s ease-out forwards;
}

.animate-slide-in-right {
  animation: slideInRight 1s ease-out forwards;
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
.animate-fade-in-up,
.animate-slide-in-left,
.animate-slide-in-right {
  opacity: 1;
  transform: none;
}

/* Card hover effects */
.bg-amber-50:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

/* Button hover effects */
button:hover {
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}
</style>