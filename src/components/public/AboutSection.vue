<template>
  <section id="about" class="py-20 bg-gradient-to-b from-blue-700 to-blue-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Enhanced Title Section -->
      <div class="text-center mb-16 animate-fade-in-up" ref="aboutTitle">
        <div class="inline-block">
          <h2 class="text-4xl md:text-5xl font-bold text-amber-900 mb-4">
            About Our Ministry
          </h2>
          <div
            class="w-24 h-1 bg-gradient-to-r from-transparent via-amber-500 to-transparent mx-auto mb-6"
          ></div>
        </div>
        <div
          class="bg-white/10 backdrop-blur-sm border border-white/20 rounded-2xl p-8 max-w-4xl mx-auto"
        >
          <p class="text-lg text-white/90 leading-relaxed font-light">
            Jesus Christ Solution Ministry is a vibrant community of believers
            dedicated to spreading God's word, love and providing spiritual
            solutions to life's challenges. We believe in the transformative
            power of faith and the importance of community support.
          </p>
        </div>
      </div>

      <!-- Mission & Vision Cards -->
      <div class="grid md:grid-cols-2 gap-8 mb-20">
        <div
          class="bg-white/95 backdrop-blur-sm p-8 lg:p-10 rounded-2xl shadow-2xl animate-slide-in-left animation-delay-300 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
          ref="missionCard"
        >
          <div
            class="bg-gradient-to-br from-amber-500 to-amber-600 w-20 h-20 rounded-full flex items-center justify-center mx-auto mb-6 shadow-lg"
          >
            <i class="fas fa-bullseye text-3xl text-white"></i>
          </div>
          <h3
            class="text-2xl lg:text-3xl font-bold text-amber-900 text-center mb-6"
          >
            Our Mission
          </h3>
          <div class="w-16 h-0.5 bg-blue-600 mx-auto mb-6"></div>
          <p class="text-gray-700 leading-relaxed text-center">
            At Jesus Christ Solution Ministry Church, our mission is to spread
            the Gospel, bring hope to the weary, and uplift souls through the
            love and teachings of Jesus Christ.
          </p>
          <div class="mt-6 pt-4 border-t border-gray-200">
            <div class="flex items-center justify-center gap-2 text-amber-700">
              <i class="fas fa-heart text-sm"></i>
              <span class="text-sm font-medium">Spreading God's Love</span>
            </div>
          </div>
        </div>

        <div
          class="bg-white/95 backdrop-blur-sm p-8 lg:p-10 rounded-2xl shadow-2xl animate-slide-in-right animation-delay-500 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
          ref="visionCard"
        >
          <div
            class="bg-gradient-to-br from-blue-500 to-blue-600 w-20 h-20 rounded-full flex items-center justify-center mx-auto mb-6 shadow-lg"
          >
            <i class="fas fa-eye text-3xl text-white"></i>
          </div>
          <h3
            class="text-2xl lg:text-3xl font-bold text-amber-900 text-center mb-6"
          >
            Our Vision
          </h3>
          <div class="w-16 h-0.5 bg-blue-600 mx-auto mb-6"></div>
          <p class="text-gray-700 leading-relaxed text-center">
            "Go into all the world and preach Good News to all creation. Whoever
            believes and is baptized will be saved." - Mark 16:15-16
          </p>
          <div class="mt-6 pt-4 border-t border-gray-200">
            <div class="flex items-center justify-center gap-2 text-blue-700">
              <i class="fas fa-globe text-sm"></i>
              <span class="text-sm font-medium">Global Gospel Mission</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Ministry Programs Section -->
      <div class="bg-gradient-to-b from-transparent to-blue-800/30 py-12">
        <div class="max-w-6xl mx-auto">
          <div class="text-center mb-12">
            <div class="inline-block">
              <h3 class="text-3xl md:text-4xl font-bold text-amber-900 mb-4">
                Ministry Programs
              </h3>
              <div
                class="w-20 h-1 bg-gradient-to-r from-transparent via-amber-500 to-transparent mx-auto mb-6"
              ></div>
            </div>
            <p class="text-lg text-white/90 font-light">
              Nurturing Faith Through Community and Service
            </p>
          </div>

          <div class="grid md:grid-cols-3 gap-8">
            <!-- Youth Ministry -->
            <div
              class="bg-white/95 backdrop-blur-sm p-8 rounded-2xl shadow-2xl animate-fade-in-up animation-delay-700 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
              ref="valueCard1"
            >
              <div
                class="bg-gradient-to-br from-red-500 to-red-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-6 shadow-lg"
              >
                <i class="fas fa-heart text-2xl text-white"></i>
              </div>
              <h4 class="text-xl font-bold text-amber-900 text-center mb-4">
                Youth Ministry
              </h4>
              <div class="bg-red-50 rounded-lg p-4 mb-4">
                <p class="text-red-800 font-medium text-center">Ages 13-25</p>
              </div>
              <p class="text-gray-700 leading-relaxed text-center">
                Guiding young people into a deeper, authentic relationship with
                Christ, fostering spiritual growth, moral formation, and a sense
                of belonging within our faith community.
              </p>
              <div class="mt-6 pt-4 border-t border-gray-200">
                <div
                  class="flex items-center justify-center gap-2 text-red-700"
                >
                  <i class="fas fa-users text-sm"></i>
                  <span class="text-sm font-medium">Youth Fellowship</span>
                </div>
              </div>
            </div>

            <!-- Sunday School Kids -->
            <div
              class="bg-white/95 backdrop-blur-sm p-8 rounded-2xl shadow-2xl animate-fade-in-up animation-delay-900 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
              ref="valueCard2"
            >
              <div
                class="bg-gradient-to-br from-green-500 to-green-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-6 shadow-lg"
              >
                <i class="fas fa-hands-helping text-2xl text-white"></i>
              </div>
              <h4 class="text-xl font-bold text-amber-900 text-center mb-4">
                Sunday School Kids
              </h4>
              <div class="bg-green-50 rounded-lg p-4 mb-4">
                <p class="text-green-800 font-medium text-center">Ages 4-12</p>
              </div>
              <p class="text-gray-700 leading-relaxed text-center">
                Where the Word of God becomes a living guide for forming
                character, building community, and inspiring lifelong
                discipleship. Children learn to love the Scriptures and carry
                God's light into the world.
              </p>
              <div class="mt-6 pt-4 border-t border-gray-200">
                <div
                  class="flex items-center justify-center gap-2 text-green-700"
                >
                  <i class="fas fa-child text-sm"></i>
                  <span class="text-sm font-medium">Children's Ministry</span>
                </div>
              </div>
            </div>

            <!-- Bible Study Group -->
            <div
              class="bg-white/95 backdrop-blur-sm p-8 rounded-2xl shadow-2xl animate-fade-in-up animation-delay-1100 hover:transform hover:scale-105 transition-all duration-500 border border-white/20"
              ref="valueCard3"
            >
              <div
                class="bg-gradient-to-br from-purple-500 to-purple-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-6 shadow-lg"
              >
                <i class="fas fa-book-open text-2xl text-white"></i>
              </div>
              <h4 class="text-xl font-bold text-amber-900 text-center mb-4">
                Bible Study Group
              </h4>
              <div class="bg-purple-50 rounded-lg p-4 mb-4">
                <p class="text-purple-800 font-medium text-center">
                  All Ages Welcome
                </p>
              </div>
              <p class="text-gray-700 leading-relaxed text-center">
                Deep dive into God's Word through interactive discussions,
                prayer, and biblical teaching that strengthens faith and builds
                spiritual understanding in our community.
              </p>
              <div class="mt-6 pt-4 border-t border-gray-200">
                <div
                  class="flex items-center justify-center gap-2 text-purple-700"
                >
                  <i class="fas fa-bible text-sm"></i>
                  <span class="text-sm font-medium">Scripture Study</span>
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
const aboutTitle = ref(null);
const missionCard = ref(null);
const visionCard = ref(null);
const valueCard1 = ref(null);
const valueCard2 = ref(null);
const valueCard3 = ref(null);

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
    aboutTitle.value,
    missionCard.value,
    visionCard.value,
    valueCard1.value,
    valueCard2.value,
    valueCard3.value,
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
  opacity: 0;
  animation: fadeInUp 2s ease-out forwards;
}

.animate-slide-in-left {
  opacity: 0;
  animation: slideInLeft 2s ease-out forwards;
}

.animate-slide-in-right {
  opacity: 0;
  animation: slideInRight 2s ease-out forwards;
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

/* Intersection observer visible state */
.animate-visible {
  opacity: 1;
  transform: translateY(0);
}

/* Enhanced shadow effects */
.shadow-2xl {
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
}

.shadow-2xl:hover {
  box-shadow: 0 35px 60px -12px rgba(0, 0, 0, 0.3);
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

  .text-3xl {
    font-size: 1.75rem;
  }

  .text-2xl {
    font-size: 1.5rem;
  }
}

@media (max-width: 480px) {
  .text-4xl {
    font-size: 2rem;
  }

  .text-5xl {
    font-size: 2.5rem;
  }

  .p-8 {
    padding: 1rem;
  }
}

/* Quote styling enhancement */
.border-t {
  transition: border-color 0.3s ease;
}

/* Program cards specific styling */
.ministry-card {
  position: relative;
  overflow: hidden;
}

.ministry-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.1),
    transparent
  );
  transition: left 0.5s;
}

.ministry-card:hover::before {
  left: 100%;
}
</style>
