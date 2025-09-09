<template>
  <section id="events" class="py-20 bg-gradient-to-b from-blue-800 to-blue-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Enhanced Title Section -->
      <div class="text-center mb-16 animate-fade-in-up" ref="eventsTitle">
        <div class="inline-block">
          <h2 class="text-4xl md:text-5xl font-bold text-amber-900 mb-4">
             Events
          </h2>
          <div
            class="w-24 h-1 bg-gradient-to-r from-transparent via-amber-500 to-transparent mx-auto mb-6"
          ></div>
        </div>
        <p class="text-lg text-white/90 font-light">
          Stay connected with our church community
        </p>
      </div>

      <!-- Enhanced Events Grid -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Youth Conference Card -->
        <div
          class="bg-white/95 backdrop-blur-sm rounded-2xl shadow-2xl overflow-hidden animate-fade-in-up animation-delay-300 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
          ref="eventCard1"
        >
          <div class="relative">
            <img
              :src="eventImage1"
              alt="Youth Conference"
              class="w-full h-48 object-cover object-top"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-black/20 via-transparent to-transparent"
            ></div>
            <!-- Date Badge -->
           
          </div>
          <div class="p-8">
            <!-- Icon -->
            <div
              class="bg-gradient-to-br from-amber-500 to-amber-600 w-12 h-12 rounded-full flex items-center justify-center mb-4 shadow-lg"
            >
              <i class="fas fa-users text-white text-lg"></i>
            </div>
            <h3 class="text-xl font-bold text-amber-900 mb-3">
              Youth Conference 2025
            </h3>
            <p class="text-gray-600 mb-6 leading-relaxed">
              A special gathering for young people to grow in faith and
              fellowship with inspiring speakers and worship.
            </p>
            <button
              class="w-full bg-gradient-to-r from-amber-800 to-amber-700 hover:from-amber-700 hover:to-amber-600 text-white px-6 py-3 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 shadow-lg"
              @click="handleLearnMore('youth-conference')"
            >
              Learn More
            </button>
          </div>
        </div>

        <!-- Community Outreach Card -->
        <div
          class="bg-white/95 backdrop-blur-sm rounded-2xl shadow-2xl overflow-hidden animate-fade-in-up animation-delay-500 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
          ref="eventCard2"
        >
          <div class="relative">
            <img
              :src="eventImage2"
              alt="Community Outreach"
              class="w-full h-48 object-cover object-top"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-black/20 via-transparent to-transparent"
            ></div>
            <!-- Date Badge -->
           
          </div>
          <div class="p-8">
            <!-- Icon -->
            <div
              class="bg-gradient-to-br from-blue-500 to-blue-600 w-12 h-12 rounded-full flex items-center justify-center mb-4 shadow-lg"
            >
              <i class="fas fa-heart text-white text-lg"></i>
            </div>
            <h3 class="text-xl font-bold text-amber-900 mb-3">
              Community Outreach Day
            </h3>
            <p class="text-gray-600 mb-6 leading-relaxed">
              Join us as we serve our community through food distribution, free
              health checkups, and prayer support.
            </p>
            <button
              class="w-full bg-gradient-to-r from-blue-600 to-blue-500 hover:from-blue-500 hover:to-blue-400 text-white px-6 py-3 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 shadow-lg"
              @click="handleVolunteer('community-outreach')"
            >
              Volunteer
            </button>
          </div>
        </div>

        <!-- Easter Celebration Card -->
        <div
          class="bg-white/95 backdrop-blur-sm rounded-2xl shadow-2xl overflow-hidden animate-fade-in-up animation-delay-700 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
          ref="eventCard3"
        >
          <div class="relative">
            <img
              :src="eventImage3"
              alt="Easter Celebration"
              class="w-full h-48 object-cover object-top"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-black/20 via-transparent to-transparent"
            ></div>
            <!-- Date Badge -->
           
          </div>
          <div class="p-8">
            <!-- Icon -->
            <div
              class="bg-gradient-to-br from-purple-600 to-purple-700 w-12 h-12 rounded-full flex items-center justify-center mb-4 shadow-lg"
            >
              <i class="fas fa-cross text-white text-lg"></i>
            </div>
            <h3 class="text-xl font-bold text-amber-900 mb-3">
              Easter Celebration
            </h3>
            <p class="text-gray-600 mb-6 leading-relaxed">
              Celebrate the resurrection of Jesus Christ with special worship
              services, music, and fellowship.
            </p>
            <button
              class="w-full bg-gradient-to-r from-amber-800 to-amber-900 hover:from-blue-500 hover:to-blue-800 text-white px-6 py-3 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 shadow-lg"
              @click="handleJoinUs('easter-celebration')"
            >
              Join Us
            </button>
          </div>
        </div>

        <!-- Visit the Hospital Card -->
        <div
          class="bg-white/95 backdrop-blur-sm rounded-2xl shadow-2xl overflow-hidden animate-fade-in-up animation-delay-900 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
          ref="eventCard4"
        >
          <div class="relative">
            <img
              :src="eventImage4"
              alt="Visit the Hospital"
              class="w-full h-48 object-cover object-top"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-black/20 via-transparent to-transparent"
            ></div>
            <!-- Date Badge -->
            
          </div>
          <div class="p-8">
            <!-- Icon -->
            <div
              class="bg-gradient-to-br from-green-500 to-green-600 w-12 h-12 rounded-full flex items-center justify-center mb-4 shadow-lg"
            >
              <i class="fas fa-hospital text-white text-lg"></i>
            </div>
            <h3 class="text-xl font-bold text-amber-900 mb-3">
              Visit the Hospital
            </h3>
            <p class="text-gray-600 mb-6 leading-relaxed">
              Join our ministry team to visit patients, pray with families, and
              bring comfort and hope to those in need of healing.
            </p>
            <button
              class="w-full bg-gradient-to-r from-amber-800 to-amber-900 hover:from-green-500 hover:to-blue-800 text-white px-6 py-3 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 shadow-lg"
              @click="handleParticipate('hospital-visit')"
            >
              Participate
            </button>
          </div>
        </div>

        <!-- Crusade Card -->
        <div
          class="bg-white/95 backdrop-blur-sm rounded-2xl shadow-2xl overflow-hidden animate-fade-in-up animation-delay-1100 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
          ref="eventCard5"
        >
          <div class="relative">
            <img
              :src="eventImage5"
              alt="Crusade"
              class="w-full h-48 object-cover object-top"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-black/20 via-transparent to-transparent"
            ></div>
            <!-- Date Badge -->
           
          </div>
          <div class="p-8">
            <!-- Icon -->
            <div
              class="bg-gradient-to-br from-red-500 to-red-600 w-12 h-12 rounded-full flex items-center justify-center mb-4 shadow-lg"
            >
              <i class="fas fa-fire text-white text-lg"></i>
            </div>
            <h3 class="text-xl font-bold text-amber-900 mb-3">
              Crusade
            </h3>
            <p class="text-gray-600 mb-6 leading-relaxed">
              A powerful evangelistic event featuring inspiring worship, prayer,
              and ministry to reach souls for Christ in our community.
            </p>
            <button
              class="w-full bg-gradient-to-r from-blue-800 to-blue-900 hover:from-red-500 hover:to-amber-800 text-white px-6 py-3 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 shadow-lg"
              @click="handleAttend('crusade')"
            >
              Attend
            </button>
          </div>
        </div>

        <!-- Women/Men Seminar Card -->
        <div
          class="bg-white/95 backdrop-blur-sm rounded-2xl shadow-2xl overflow-hidden animate-fade-in-up animation-delay-1300 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
          ref="eventCard6"
        >
          <div class="relative">
            <img
              :src="eventImage6"
              alt="Women/Men Seminar"
              class="w-full h-48 object-cover object-top"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-black/20 via-transparent to-transparent"
            ></div>
            <!-- Date Badge -->
           
          </div>
          <div class="p-8">
            <!-- Icon -->
            <div
              class="bg-gradient-to-br from-indigo-500 to-indigo-600 w-12 h-12 rounded-full flex items-center justify-center mb-4 shadow-lg"
            >
              <i class="fas fa-users-cog text-white text-lg"></i>
            </div>
            <h3 class="text-xl font-bold text-amber-900 mb-3">
              Women/Men Seminar
            </h3>
            <p class="text-gray-600 mb-6 leading-relaxed">
              Empowering seminars designed for both men and women to strengthen
              relationships, faith, and personal growth in Christ.
            </p>
            <button
              class="w-full bg-gradient-to-r from-amber-800 to-amber-900 hover:from-indigo-500 hover:to-blue-800 text-white px-6 py-3 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 shadow-lg"
              @click="handleRegister('seminar')"
            >
              Register
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref, onMounted } from "vue";

// Template refs
const eventsTitle = ref(null);
const eventCard1 = ref(null);
const eventCard2 = ref(null);
const eventCard3 = ref(null);
const eventCard4 = ref(null);
const eventCard5 = ref(null);
const eventCard6 = ref(null);

// Event images
const eventImage1 =
  "https://readdy.ai/api/search-image?query=young%20people%20gathering%20in%20modern%20church%20setting%20with%20warm%20lighting%20and%20contemporary%20worship%20atmosphere%20featuring%20brown%20and%20blue%20color%20scheme%20for%20youth%20conference%20event&width=400&height=300&seq=event001&orientation=landscape";
const eventImage2 =
  "https://readdy.ai/api/search-image?query=community%20volunteers%20serving%20food%20and%20helping%20people%20in%20outdoor%20setting%20with%20warm%20brown%20and%20soft%20blue%20tones%20showing%20church%20outreach%20and%20charity%20work%20in%20action&width=400&height=300&seq=event002&orientation=landscape";
const eventImage3 =
  "https://readdy.ai/api/search-image?query=beautiful%20easter%20celebration%20setup%20with%20cross%20flowers%20and%20warm%20lighting%20in%20church%20sanctuary%20featuring%20brown%20and%20blue%20color%20palette%20for%20resurrection%20sunday%20worship%20service&width=400&height=300&seq=event003&orientation=landscape";
const eventImage4 =
  "https://readdy.ai/api/search-image?query=volunteers%20entertaining%20children%20in%20colorful%20hospital%20ward%20with%20toys%20books%20and%20cheerful%20decorations%20creating%20joyful%20healing%20environment&width=400&height=225&seq=hosp002&orientation=landscape";
const eventImage5 =
  "https://readdy.ai/api/search-image?query=energetic%20youth%20rally%20in%20sports%20arena%20with%20contemporary%20stage%20lighting%20young%20people%20worshipping%20and%20modern%20sound%20equipment&width=400&height=225&seq=crus002&orientation=landscape";
    
const eventImage6 =
  "https://readdy.ai/api/search-image?query=men%20attending%20brotherhood%20summit%20in%20community%20center%20with%20workshop%20tables%20and%20mentorship%20discussion%20groups%20in%20professional%20setting&width=400&height=225&seq=men001&orientation=landscape";
// Event handlers
const handleLearnMore = (eventType: string) => {
  console.log(`Learn more about: ${eventType}`);
  // Add your navigation or modal logic here
};

const handleVolunteer = (eventType: string) => {
  console.log(`Volunteer for: ${eventType}`);
  // Add your volunteer registration logic here
};

const handleJoinUs = (eventType: string) => {
  console.log(`Join us for: ${eventType}`);
  // Add your event registration logic here
};

const handleParticipate = (eventType: string) => {
  console.log(`Participate in: ${eventType}`);
  // Add your participation logic here
};

const handleAttend = (eventType: string) => {
  console.log(`Attend: ${eventType}`);
  // Add your attendance logic here
};

const handleRegister = (eventType: string) => {
  console.log(`Register for: ${eventType}`);
  // Add your registration logic here
};

// Intersection observer for scroll-triggered animations
onMounted(() => {
  const observerOptions = {
    threshold: 0.1,
    rootMargin: "0px 0px -50px 0px",
  };

  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        entry.target.classList.add("animate-visible");
      }
    });
  }, observerOptions);

  // Observe all animated elements
  const elements = [
    eventsTitle.value,
    eventCard1.value,
    eventCard2.value,
    eventCard3.value,
    eventCard4.value,
    eventCard5.value,
    eventCard6.value,
  ];

  elements.forEach((el) => {
    if (el) observer.observe(el);
  });
});
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

/* Animation classes */
.animate-fade-in-up {
  opacity: 0;
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

.animation-delay-900 {
  animation-delay: 0.9s;
}

.animation-delay-1100 {
  animation-delay: 1.1s;
}

.animation-delay-1300 {
  animation-delay: 1.3s;
}

/* Intersection observer visible state */
.animate-visible {
  opacity: 1;
  transform: translateY(0);
}

/* Enhanced card hover effects */
.bg-white\/95:hover {
  transform: translateY(-8px) scale(1.02);
  box-shadow: 0 25px 50px rgba(0, 0, 0, 0.25);
  transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
}

/* Icon container hover effects */
.rounded-full:hover {
  transform: rotate(10deg) scale(1.1);
  transition: transform 0.3s ease;
}

/* Backdrop blur support */
.backdrop-blur-sm {
  backdrop-filter: blur(4px);
}

/* Enhanced shadow effects */
.shadow-2xl {
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
}

.shadow-2xl:hover {
  box-shadow: 0 35px 60px -12px rgba(0, 0, 0, 0.3);
}

/* Button hover effects */
button:hover {
  transform: translateY(-2px) scale(1.05);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
}

/* Gradient button animations */
.bg-gradient-to-r:hover {
  background-size: 200% 200%;
  animation: gradient 2s ease infinite;
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .p-8 {
    padding: 1.5rem;
  }

  .text-4xl {
    font-size: 2rem;
  }
}
</style>