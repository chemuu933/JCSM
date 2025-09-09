<template>
  <section id="services" class="py-20 bg-gradient-to-b from-blue-800 to-blue-700">
    <!-- Service Times Section -->
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16 animate-fade-in-up" ref="servicesTitle">
        <div class="inline-block">
          <h2 class="text-4xl md:text-5xl font-bold text-amber-900 mb-4">Service Time</h2>
          <div class="w-24 h-1 bg-gradient-to-r from-transparent via-amber-500 to-transparent mx-auto mb-6"></div>
        </div>
        <p class="text-lg text-white/90 font-light">Join us for worship and fellowship</p>
      </div>

      <!-- Enhanced Service Cards Grid -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Sunday Morning Service -->
        <div
          class="bg-white/95 backdrop-blur-sm p-8 rounded-2xl text-center shadow-2xl animate-fade-in-up animation-delay-300 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
          ref="serviceCard1"
        >
          <div class="bg-gradient-to-br from-amber-500 to-amber-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-6 shadow-lg">
            <i class="fas fa-sun text-2xl text-white"></i>
          </div>
          <h3 class="text-xl font-bold text-amber-900 mb-3">Sunday Morning Service</h3>
          <div class="bg-blue-50 rounded-lg p-4 mb-4">
            <p class="text-blue-800 font-semibold text-lg">9:30 AM - 12:00 PM</p>
          </div>
          <p class="text-gray-600 leading-relaxed">
            Main worship service with praise, worship, and biblical teaching that nourishes the soul
          </p>
          <div class="mt-6 pt-4 border-t border-gray-200">
            <div class="flex items-center justify-center gap-2 text-amber-700">
              <i class="fas fa-music text-sm"></i>
              <span class="text-sm font-medium">Worship & Teaching</span>
            </div>
          </div>
        </div>

        <!-- Friday Praise & Worship -->
        <div
          class="bg-white/95 backdrop-blur-sm p-8 rounded-2xl text-center shadow-2xl animate-fade-in-up animation-delay-500 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
          ref="serviceCard2"
        >
          <div class="bg-gradient-to-br from-blue-500 to-blue-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-6 shadow-lg">
            <i class="fas fa-moon text-2xl text-white"></i>
          </div>
          <h3 class="text-xl font-bold text-amber-900 mb-3">Friday Praise & Worship</h3>
          <div class="bg-amber-50 rounded-lg p-4 mb-4">
            <p class="text-amber-800 font-semibold text-lg">5:00 PM - 6:00 PM</p>
          </div>
          <p class="text-gray-600 leading-relaxed">
            Evening worship with prayer and communion that brings hearts together in unity
          </p>
          <div class="mt-6 pt-4 border-t border-gray-200">
            <div class="flex items-center justify-center gap-2 text-blue-700">
              <i class="fas fa-praying-hands text-sm"></i>
              <span class="text-sm font-medium">Prayer & Communion</span>
            </div>
          </div>
        </div>

        <!-- Wednesday Prayers -->
        <div
          class="bg-white/95 backdrop-blur-sm p-8 rounded-2xl text-center shadow-2xl animate-fade-in-up animation-delay-700 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
          ref="serviceCard3"
        >
          <div class="bg-gradient-to-br from-amber-600 to-amber-700 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-6 shadow-lg">
            <i class="fas fa-book-open text-2xl text-white"></i>
          </div>
          <h3 class="text-xl font-bold text-amber-900 mb-3">Wednesday Prayers</h3>
          <div class="bg-blue-50 rounded-lg p-4 mb-4">
            <p class="text-blue-800 font-semibold text-lg">5:30 PM - 6:30 PM</p>
          </div>
          <p class="text-gray-600 leading-relaxed">
            Powerful prayer sessions that strengthen faith and build community bonds
          </p>
          <div class="mt-6 pt-4 border-t border-gray-200">
            <div class="flex items-center justify-center gap-2 text-amber-700">
              <i class="fas fa-hands text-sm"></i>
              <span class="text-sm font-medium">Community Prayer</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Enhanced Founder Section (keeping your existing design) -->
    <div class="mt-24 bg-gradient-to-b from-transparent to-blue-800/30 py-12">
      <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16 animate-fade-in-up" ref="founderTitle">
          <div class="inline-block">
            <h2 class="text-4xl md:text-5xl font-bold text-amber-900 mb-4">
              Founder
            </h2>
            <div
              class="w-24 h-1 bg-gradient-to-r from-transparent via-amber-500 to-transparent mx-auto mb-6"
            ></div>
          </div>
          <p class="text-lg text-white/90 font-light">
            Leading with Vision and Faith
          </p>
        </div>

        <div
          class="bg-white/95 backdrop-blur-sm rounded-2xl shadow-2xl overflow-hidden animate-fade-in-up animation-delay-300"
          ref="founderContent"
        >
          <div class="flex flex-col lg:flex-row">
            <!-- Image Container -->
            <div class="lg:w-2/5 relative overflow-hidden">
              <div class="aspect-[4/5] lg:aspect-auto lg:h-full relative">
                <img
                  :src="founderImageUrl"
                  alt="Dr. Emily Cheposero Tumwet - Founder"
                  class="w-full h-full object-cover object-center transition-transform duration-700 hover:scale-105"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/20 via-transparent to-transparent"
                ></div>
              </div>
            </div>

            <!-- Content Container -->
            <div class="lg:w-3/5 p-8 lg:p-12 flex flex-col justify-center">
              <div class="space-y-6">
                <div>
                  <h3
                    class="text-2xl lg:text-3xl font-bold text-amber-900 mb-2"
                  >
                    Dr. Emily Cheposero Tumwet
                  </h3>
                  <div class="w-16 h-0.5 bg-blue-600 mb-6"></div>
                </div>

                <div class="space-y-4 text-gray-700 leading-relaxed">
                  <p class="text-base lg:text-lg">
                    With a passion for ministry and a heart for God's people,
                    Dr. Emily Cheposero Tumwet leads Jesus Christ Solution
                    Ministry Church with wisdom, grace, and an unwavering
                    commitment to spreading the Word of God.
                  </p>

                  <p class="text-base lg:text-lg">
                    She is a devoted servant of Christ, dedicated to guiding
                    believers in their spiritual journey and empowering them to
                    live according to God's purpose. Through her powerful
                    teachings, heartfelt prayers, and deep biblical insights,
                    she continues to transform lives and bring hope to many.
                  </p>

                  <div
                    class="bg-blue-50 border-l-4 border-blue-600 p-4 rounded-r-lg"
                  >
                    <p class="text-blue-800 italic font-medium">
                      "Her leadership is centered on faith, love, and the power
                      of the Holy Spirit to bring healing and restoration to all
                      who seek Christ."
                    </p>
                  </div>
                </div>

                <!-- Optional: Add contact or social links -->
                <div class="pt-4">
                  <div class="flex items-center gap-4">
                    <div class="flex items-center gap-2 text-amber-900">
                      <i class="fas fa-cross text-lg"></i>
                      <span class="font-semibold">Ministry Leader</span>
                    </div>
                    <div class="flex items-center gap-2 text-blue-600">
                      <i class="fas fa-book text-lg"></i>
                      <span class="font-semibold">Biblical Teacher</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref, onMounted } from "vue";

// Template refs
const servicesTitle = ref(null);
const serviceCard1 = ref(null);
const serviceCard2 = ref(null);
const serviceCard3 = ref(null);
const founderTitle = ref(null);
const founderContent = ref(null);

import founderImageUrl from "../../assets/jcsm2.jpg";

// Optional: Add intersection observer for scroll-triggered animations
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
    servicesTitle.value,
    serviceCard1.value,
    serviceCard2.value,
    serviceCard3.value,
    founderTitle.value,
    founderContent.value,
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

/* Enhanced founder section styles */
.founder-card {
  background: linear-gradient(
    135deg,
    rgba(255, 255, 255, 0.95) 0%,
    rgba(255, 255, 255, 0.9) 100%
  );
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
}

/* Image container enhancements */
.aspect-\[4\/5\] {
  aspect-ratio: 4/5;
}

/* Responsive adjustments */
@media (max-width: 1024px) {
  .lg\:aspect-auto {
    aspect-ratio: 4/3;
  }
}

@media (max-width: 768px) {
  .flex {
    gap: 1rem;
  }

  .text-3xl {
    font-size: 1.5rem;
  }

  .aspect-\[4\/5\] {
    aspect-ratio: 3/4;
  }

  .grid {
    grid-template-columns: 1fr;
  }

  .p-8 {
    padding: 1.5rem;
  }
}

/* Hover effects for the founder card */
.bg-white\/95:hover {
  transform: translateY(-2px);
  box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
  transition: all 0.4s ease;
}

/* Quote styling enhancement */
.border-l-4 {
  transition: border-color 0.3s ease;
}

.border-l-4:hover {
  border-color: #1d4ed8;
}

/* Service card specific enhancements */
.service-card-hover {
  position: relative;
  overflow: hidden;
}

.service-card-hover::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
  transition: left 0.5s;
}

.service-card-hover:hover::before {
  left: 100%;
}

/* Gradient text for service times */
.service-time-gradient {
  background: linear-gradient(135deg, #f59e0b, #d97706);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* Enhanced shadow effects */
.shadow-2xl {
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
}

.shadow-2xl:hover {
  box-shadow: 0 35px 60px -12px rgba(0, 0, 0, 0.3);
}
</style>