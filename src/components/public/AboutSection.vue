<template>
  <section id="about" class="py-20 bg-blue-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16 animate-fade-in-up" ref="aboutTitle">
        <h2 class="text-4xl font-bold text-orange-600 mb-6">
          About Our Ministry
        </h2>
        <p class="text-lg text-white max-w-3xl mx-auto leading-relaxed">
          Jesus Christ Solution Ministry is a vibrant community of believers
          dedicated to spreading God's love and providing spiritual solutions to
          life's challenges. We believe in the transformative power of faith and
          the importance of community support.
        </p>
      </div>

      <div class="grid md:grid-cols-2 gap-12 mb-16">
        <div
          class="bg-orange-600 p-8 rounded-lg shadow-md animate-slide-in-left animation-delay-300"
          ref="missionCard"
        >
          <div
            class="w-16 h-16 bg-blue-200 rounded-full flex items-center justify-center mx-auto mb-4"
          >
            <i class="fas fa-bullseye text-2xl text-amber-800"></i>
          </div>
          <h3 class="text-2xl font-bold text-white text-center mb-4">
            Our Mission
          </h3>
          <p class="text-stone-900 leading-relaxed">
            At Jesus Christ Solution Ministry Church, our mission is to spread
            the Gospel, bring hope to the weary, and uplift souls through the
            love and teachings of Jesus Christ.
          </p>
        </div>

        <div
          class="bg-orange-600 p-8 rounded-lg shadow-md animate-slide-in-right animation-delay-500"
          ref="visionCard"
        >
          <div
            class="w-16 h-16 bg-blue-200 rounded-full flex items-center justify-center mx-auto mb-4"
          >
            <i class="fas fa-eye text-2xl text-amber-800"></i>
          </div>
          <h3 class="text-2xl font-bold text-white text-center mb-4">
            Our Vision
          </h3>
          <p class="text-gray-900 leading-relaxed">
            Go into all the world and preach GoodNews to all creation,Whoever
            belleves will be saved
          </p>
        </div>
      </div>

      <div class="grid md:grid-cols-3 gap-8">
        <div
          class="text-center p-6 bg-orange-600 rounded-lg shadow-md animate-fade-in-up animation-delay-700"
          ref="valueCard1"
        >
          <div
            class="w-16 h-16 bg-blue-200 rounded-full flex items-center justify-center mx-auto mb-4"
          >
            <i class="fas fa-heart text-2xl text-amber-800"></i>
          </div>
          <h3 class="text-xl font-semibold text-white mb-3">
            Youth Ministry
          </h3>
          <p class="text-gray-900">
            Our Youth Ministry is dedicated to guiding young people into a
            deeper, authentic relationship with Christ, fostering spiritual
            growth, moral formation, and a sense of belonging within our faith
            community
          </p>
        </div>

        <div
          class="text-center p-6 bg-orange-600 rounded-lg shadow-md animate-fade-in-up animation-delay-900"
          ref="valueCard2"
        >
          <div
            class="w-16 h-16 bg-blue-200 rounded-full flex items-center justify-center mx-auto mb-4"
          >
            <i class="fas fa-hands-helping text-2xl text-amber-800"></i>
          </div>
          <h3 class="text-xl font-semibold text-white mb-3">
            Sunday Shool Kids
          </h3>
          <p class="text-gray-900">
            Here, the Word of God becomes a living guide—not just for teaching,
            but for forming character, building community, and inspiring
            lifelong discipleship. We joyfully welcome children into an
            environment where they learn to love the Scriptures, live out their
            faith, and carry God’s light into their families, friendships, and
            the world.
          </p>
        </div>

        <div
          class="text-center p-6 bg-orange-600 rounded-lg shadow-md animate-fade-in-up animation-delay-1100"
          ref="valueCard3"
        >
          <div
            class="w-16 h-16 bg-blue-200 rounded-full flex items-center justify-center mx-auto mb-4"
          >
            <i class="fas fa-pray text-2xl text-amber-800"></i>
          </div>
          <h3 class="text-xl font-semibold text-white mb-3">
            Bible Study Group
          </h3>
          <p class="text-gray-900">
            We provide opportunities for spiritual development through worship,
            prayer, and biblical teaching.
          </p>
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

// Optional: Add intersection observer for scroll-triggered animations
onMounted(() => {
  // You can add scroll-triggered animations here if needed
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
    opacity: 1;
    transform: translateY(30px);
  }
  to {
    opacity: 3;
    transform: translateY(0);
  }
}

@keyframes slideInLeft {
  from {
    opacity: 1;
    transform: translateX(-50px);
  }
  to {
    opacity: 2;
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  from {
    opacity: 1;
    transform: translateX(50px);
  }
  to {
    opacity: 2;
    transform: translateX(0);
  }
}

/* Animation classes */
.animate-fade-in-up {
  animation: fadeInUp 2s ease-out forwards;
}

.animate-slide-in-left {
  animation: slideInLeft 2s ease-out forwards;
}

.animate-slide-in-right {
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

/* Fallback visibility */
.animate-fade-in-up,
.animate-slide-in-left,
.animate-slide-in-right {
  opacity: 2s; /* Ensures content is visible even without animation */
}

/* Optional: For scroll-triggered animations */
.animate-visible {
  animation-play-state: running !important;
}
</style>
