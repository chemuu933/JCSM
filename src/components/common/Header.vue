<template>
  <nav
    class="fixed top-0 left-0 right-0 bg-white/95 backdrop-blur-md shadow-lg z-50 border-b border-blue-100/50 transition-all duration-300"
    :class="{ 'bg-white/98 shadow-xl': isScrolled }"
  >
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-20">
        <!-- Enhanced Logo Section -->
        <div
          class="flex-shrink-0 flex items-center gap-4 group cursor-pointer"
          @click="scrollToTop"
        >
          <div class="relative">
            <img
                :src="founderImageUrl"
                alt="Jesus Solution Ministry Logo"
                class="w-20 h-20 object-contain group-hover:scale-110 transition-transform duration-300"
              />
            <!-- Decorative ring -->
            <div
              class="absolute inset-0 rounded-full border-2 border-blue-200 opacity-0 group-hover:opacity-100 scale-110 group-hover:scale-125 transition-all duration-300"
            ></div>
          </div>
          <div class="hidden sm:block">
            <h1
              class="text-xl lg:text-2xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-amber-800 to-amber-600 leading-tight"
            >
              JESUS SOLUTION
              <br />
              <span class="text-lg lg:text-xl text-blue-700 font-semibold"
                >MINISTRY</span
              >
            </h1>
          </div>
          <!-- Mobile Logo Text -->
          <div class="block sm:hidden">
            <h1
              class="text-lg font-bold text-transparent bg-clip-text bg-gradient-to-r from-amber-800 to-amber-600"
            >
              JSM
            </h1>
          </div>
        </div>

        <!-- Desktop Navigation -->
        <div class="hidden lg:block">
          <div class="flex items-center space-x-1">
            <a
              v-for="item in navigationItems"
              :key="item.id"
              :href="item.href"
              class="relative px-4 py-2 text-sm font-semibold text-amber-800 hover:text-blue-600 transition-all duration-300 rounded-lg hover:bg-blue-50 group"
              :class="{ 'text-blue-600 bg-blue-50': activeSection === item.id }"
              @click="scrollToSection(item.id)"
            >
              <div class="flex items-center gap-2">
                <i
                  :class="item.icon"
                  class="text-sm group-hover:scale-110 transition-transform duration-200"
                ></i>
                <span class="relative">
                  {{ item.name }}
                  <!-- Active indicator -->
                  <div
                    class="absolute -bottom-1 left-0 w-0 h-0.5 bg-gradient-to-r from-blue-500 to-amber-500 group-hover:w-full transition-all duration-300"
                    :class="{ 'w-full': activeSection === item.id }"
                  ></div>
                </span>
              </div>
            </a>
          </div>
        </div>

        <!-- Call to Action Button (Desktop) -->
        <div class="hidden lg:block">
          <button
            class="bg-gradient-to-r from-amber-800 to-amber-900 hover:from-blue-700 hover:to-blue-800 text-white px-6 py-2.5 rounded-full font-semibold text-sm shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105 flex items-center gap-2"
            @click="scrollToSection('offering')"
          >
            <i class="fas fa-heart text-sm"></i>
            <span>Give Today</span>
          </button>
        </div>

        <!-- Mobile/Tablet Menu Button -->
        <div class="lg:hidden">
          <button
            @click="mobileMenuOpen = !mobileMenuOpen"
            class="relative w-10 h-10 bg-gradient-to-br from-blue-500 to-blue-600 hover:from-blue-600 hover:to-blue-700 rounded-lg flex items-center justify-center shadow-lg hover:shadow-xl transition-all duration-300 group"
            :class="{ 'rotate-90': mobileMenuOpen }"
          >
            <div class="relative w-5 h-5">
              <span
                class="absolute w-5 h-0.5 bg-white rounded-full transition-all duration-300 group-hover:bg-amber-200"
                :class="mobileMenuOpen ? 'rotate-45 top-2' : 'top-1'"
              ></span>
              <span
                class="absolute w-5 h-0.5 bg-white rounded-full top-2 transition-all duration-300 group-hover:bg-amber-200"
                :class="{ 'opacity-0': mobileMenuOpen }"
              ></span>
              <span
                class="absolute w-5 h-0.5 bg-white rounded-full transition-all duration-300 group-hover:bg-amber-200"
                :class="mobileMenuOpen ? '-rotate-45 top-2' : 'top-3'"
              ></span>
            </div>
          </button>
        </div>
      </div>

      <!-- Enhanced Mobile Navigation -->
      <div
        class="lg:hidden overflow-hidden transition-all duration-300"
        :class="mobileMenuOpen ? 'max-h-96 opacity-100' : 'max-h-0 opacity-0'"
      >
        <div
          class="py-4 space-y-1 bg-gradient-to-b from-blue-50 to-white rounded-b-2xl shadow-inner border-t border-blue-100/50 mx-4 mb-4"
        >
          <a
            v-for="item in navigationItems"
            :key="item.id"
            :href="item.href"
            class="flex items-center gap-3 px-6 py-3 text-base font-medium text-gray-700 hover:text-blue-600 hover:bg-white rounded-lg transition-all duration-300 group mx-2"
            :class="{
              'text-blue-600 bg-white shadow-sm': activeSection === item.id,
            }"
            @click="handleMobileNavClick(item.id)"
          >
            <div
              class="w-8 h-8 bg-gradient-to-br from-blue-100 to-blue-200 rounded-lg flex items-center justify-center group-hover:from-blue-200 group-hover:to-blue-300 transition-all duration-200"
            >
              <i :class="item.icon" class="text-blue-600 text-sm"></i>
            </div>
            <span
              class="group-hover:translate-x-1 transition-transform duration-200"
              >{{ item.name }}</span
            >
          </a>

          <!-- Mobile CTA -->
          <div class="px-2 pt-4">
            <button
              class="w-full bg-gradient-to-r from-amber-600 to-amber-500 hover:from-amber-500 hover:to-amber-400 text-white px-6 py-3 rounded-xl font-semibold shadow-lg hover:shadow-xl transition-all duration-300 flex items-center justify-center gap-2"
              @click="handleMobileNavClick('offering')"
            >
              <i class="fas fa-heart"></i>
              <span>Give Today</span>
            </button>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script lang="ts" setup>
import { ref, onMounted, onUnmounted } from "vue";
import founderImageUrl from "../../assets/logo.png";

// Reactive data
const mobileMenuOpen = ref(false);
const isScrolled = ref(false);
const activeSection = ref("home");

// Navigation items
const navigationItems = [
  { id: "home", name: "Home", href: "#home", icon: "fas fa-home" },
  { id: "about", name: "About", href: "#about", icon: "fas fa-heart" },
  {
    id: "services",
    name: "Services",
    href: "#services",
    icon: "fas fa-church",
  },
  {
    id: "events",
    name: "Events",
    href: "#events",
    icon: "fas fa-calendar-alt",
  },
];

// Scroll to section functionality
const scrollToSection = (sectionId: string) => {
  const element = document.getElementById(sectionId);
  if (element) {
    const navHeight = 80; // Account for fixed nav height
    const elementPosition =
      element.getBoundingClientRect().top + window.pageYOffset;
    const offsetPosition = elementPosition - navHeight;

    window.scrollTo({
      top: offsetPosition,
      behavior: "smooth",
    });
  }
};

// Scroll to top
const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
  activeSection.value = "home";
};

// Handle mobile navigation click
const handleMobileNavClick = (sectionId: string) => {
  scrollToSection(sectionId);
  mobileMenuOpen.value = false;
};

// Handle scroll events
const handleScroll = () => {
  isScrolled.value = window.scrollY > 20;

  // Update active section based on scroll position
  const sections = ["home", "about", "services", "events", "offering"];
  const navHeight = 100;

  for (const sectionId of sections) {
    const element = document.getElementById(sectionId);
    if (element) {
      const rect = element.getBoundingClientRect();
      if (rect.top <= navHeight && rect.bottom >= navHeight) {
        activeSection.value = sectionId;
        break;
      }
    }
  }
};

// Close mobile menu when clicking outside
const handleClickOutside = (event: Event) => {
  const nav = document.querySelector("nav");
  if (nav && !nav.contains(event.target as Node)) {
    mobileMenuOpen.value = false;
  }
};

// Lifecycle hooks
onMounted(() => {
  window.addEventListener("scroll", handleScroll);
  document.addEventListener("click", handleClickOutside);
  handleScroll(); // Set initial state
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
  document.removeEventListener("click", handleClickOutside);
});
</script>

<style scoped>
/* Enhanced gradient text */
.bg-clip-text {
  -webkit-background-clip: text;
  background-clip: text;
}

/* Backdrop blur support */
.backdrop-blur-md {
  backdrop-filter: blur(12px);
}

/* Smooth transitions for all elements */
* {
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

/* Enhanced button hover effects */
button:hover {
  transform: translateY(-1px);
}

/* Navigation link animations */
a:hover {
  transform: translateY(-1px);
}

/* Mobile menu animation */
.max-h-96 {
  max-height: 24rem;
}

.max-h-0 {
  max-height: 0;
}

/* Smooth scroll behavior */
html {
  scroll-behavior: smooth;
}

/* Logo hover animation */
.group:hover img {
  animation: logoGlow 1s ease-in-out infinite alternate;
}

@keyframes logoGlow {
  from {
    filter: drop-shadow(0 0 5px rgba(255, 255, 255, 0.5));
  }
  to {
    filter: drop-shadow(0 0 15px rgba(255, 255, 255, 0.8));
  }
}

/* Hamburger menu animation */
.rotate-90 {
  transform: rotate(90deg);
}

/* Active section indicator */
.bg-gradient-to-r {
  background-size: 200% 100%;
  animation: gradientShift 3s ease infinite;
}

@keyframes gradientShift {
  0%,
  100% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
}

/* Enhanced shadow effects */
.shadow-lg {
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1),
    0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

.shadow-xl {
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1),
    0 10px 10px -5px rgba(0, 0, 0, 0.04);
}

/* Mobile responsiveness */
@media (max-width: 1024px) {
  .lg\:text-2xl {
    font-size: 1.5rem;
  }

  .lg\:text-xl {
    font-size: 1.25rem;
  }
}

@media (max-width: 640px) {
  .h-20 {
    height: 4.5rem;
  }

  .px-4 {
    padding-left: 1rem;
    padding-right: 1rem;
  }
}

/* Focus states for accessibility */
a:focus,
button:focus {
  outline: 2px solid #3b82f6;
  outline-offset: 2px;
}

/* Prevent text selection on interactive elements */
button,
.cursor-pointer {
  user-select: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
}

/* Enhanced mobile menu styling */
.space-y-1 > * + * {
  margin-top: 0.25rem;
}

.mx-2 {
  margin-left: 0.5rem;
  margin-right: 0.5rem;
}

/* Loading animation for better UX */
@keyframes fadeInDown {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fadeInDown {
  animation: fadeInDown 0.3s ease-out;
}
</style>
