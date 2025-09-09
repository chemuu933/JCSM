<template>
  <footer
    class="bg-gradient-to-b from-amber-800 to-amber-900 text-white relative overflow-hidden"
  >
    <div class="relative z-10 py-16">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <!-- Main Footer Content -->
        <div class="grid md:grid-cols-4 gap-8 mb-12">
          <!-- Church Info -->
          <div class="md:col-span-1">
            <div class="mb-6">
              <div
                class="bg-gradient-to-br from-blue-500 to-blue-600 w-16 h-16 rounded-full flex items-center justify-center mb-4 shadow-lg overflow-hidden"
              >
                <img
                  :src="founderImageUrl"
                  alt="Jesus Solution Ministry Logo"
                  class="w-12 h-12 object-contain"
                />
              </div>
              <h3 class="text-2xl font-bold text-white mb-2">
                Jesus Solution Ministry
              </h3>
              <p class="text-white text-sm leading-relaxed">
                Transforming lives through the power of God's love and grace.
                Join us in our mission to spread hope and healing.
              </p>
            </div>
          </div>

          <!-- Contact Info -->
          <div>
            <h3 class="text-xl font-semibold mb-6 text-white flex items-center">
              <div
                class="bg-gradient-to-br from-amber-500 to-amber-600 w-8 h-8 rounded-full flex items-center justify-center mr-3"
              >
                <i class="fas fa-phone text-white text-sm"></i>
              </div>
              Contact Us
            </h3>
            <div class="space-y-4">
              <div class="flex items-start group">
                <div
                  class="bg-white/10 backdrop-blur-sm w-8 h-8 rounded-lg flex items-center justify-center mr-3 group-hover:bg-white/20 transition-colors"
                >
                  <i class="fas fa-map-marker-alt text-amber-300 text-sm"></i>
                </div>
                <div>
                  <p class="text-white text-sm leading-relaxed">
                    Rafiki Center<br />
                    <span class="text-amber-200"
                      ></span
                    >
                  </p>
                </div>
              </div>

              <div
                class="flex items-center group cursor-pointer"
                @click="callPhone"
              >
                <div
                  class="bg-white/10 backdrop-blur-sm w-8 h-8 rounded-lg flex items-center justify-center mr-3 group-hover:bg-white/20 transition-colors"
                >
                  <i class="fas fa-phone text-green-400 text-sm"></i>
                </div>
                <p
                  class="text-white text-sm group-hover:text-white transition-colors"
                >
                  0792665651
                </p>
              </div>

              <div
                class="flex items-center group cursor-pointer"
                @click="sendEmail"
              >
                <div
                  class="bg-white/10 backdrop-blur-sm w-8 h-8 rounded-lg flex items-center justify-center mr-3 group-hover:bg-white/20 transition-colors"
                >
                  <i class="fas fa-envelope text-blue-400 text-sm"></i>
                </div>
                <p
                  class="text-white text-sm group-hover:text-white transition-colors"
                >
                  info@jcsministry.org
                </p>
              </div>
            </div>
          </div>

          <!-- Quick Links -->
          <div>
            <h3 class="text-xl font-semibold mb-6 text-white flex items-center">
              <div
                class="bg-gradient-to-br from-blue-500 to-blue-600 w-8 h-8 rounded-full flex items-center justify-center mr-3"
              >
                <i class="fas fa-link text-white text-sm"></i>
              </div>
              Quick Links
            </h3>
            <div class="space-y-3">
              <a
                href="#home"
                class="flex items-center text-white hover:text-white transition-all duration-300 group text-sm"
                @click="scrollToSection('home')"
              >
                <div
                  class="w-2 h-2 bg-amber-500 rounded-full mr-3 group-hover:scale-125 transition-transform"
                ></div>
                <span class="group-hover:translate-x-1 transition-transform"
                  >Home</span
                >
              </a>
              <a
                href="#about"
                class="flex items-center text-white hover:text-white transition-all duration-300 group text-sm"
                @click="scrollToSection('about')"
              >
                <div
                  class="w-2 h-2 bg-amber-500 rounded-full mr-3 group-hover:scale-125 transition-transform"
                ></div>
                <span class="group-hover:translate-x-1 transition-transform"
                  >About Us</span
                >
              </a>
              <a
                href="#services"
                class="flex items-center text-white hover:text-white transition-all duration-300 group text-sm"
                @click="scrollToSection('services')"
              >
                <div
                  class="w-2 h-2 bg-amber-500 rounded-full mr-3 group-hover:scale-125 transition-transform"
                ></div>
                <span class="group-hover:translate-x-1 transition-transform"
                  >Services</span
                >
              </a>
              <a
                href="#events"
                class="flex items-center text-white hover:text-white transition-all duration-300 group text-sm"
                @click="scrollToSection('events')"
              >
                <div
                  class="w-2 h-2 bg-amber-500 rounded-full mr-3 group-hover:scale-125 transition-transform"
                ></div>
                <span class="group-hover:translate-x-1 transition-transform"
                  >Events</span
                >
              </a>
              <a
                href="#offering"
                class="flex items-center text-white hover:text-white transition-all duration-300 group text-sm"
                @click="scrollToSection('offering')"
              >
                <div
                  class="w-2 h-2 bg-amber-500 rounded-full mr-3 group-hover:scale-125 transition-transform"
                ></div>
                <span class="group-hover:translate-x-1 transition-transform"
                  >Offering</span
                >
              </a>
            </div>
          </div>

          <!-- Social Media & Ministry Hours -->
          <div>
            <h3 class="text-xl font-semibold mb-6 text-white flex items-center">
              <div
                class="bg-gradient-to-br from-amber-500 to-amber-600 w-8 h-8 rounded-full flex items-center justify-center mr-3"
              >
                <i class="fas fa-heart text-white text-sm"></i>
              </div>
              Connect & Visit
            </h3>

            <!-- Social Media -->
            <div class="mb-6">
              <p class="text-white text-sm mb-3">Follow Us</p>
              <div class="flex space-x-3">
                <a
                  href="#"
                  class="bg-white/10 backdrop-blur-sm w-10 h-10 rounded-lg flex items-center justify-center hover:bg-blue-600 transition-all duration-300 transform hover:scale-110 hover:-translate-y-1"
                  title="Facebook"
                >
                  <i class="fab fa-facebook text-white text-lg"></i>
                </a>
                <a
                  href="#"
                  class="bg-white/10 backdrop-blur-sm w-10 h-10 rounded-lg flex items-center justify-center hover:bg-red-600 transition-all duration-300 transform hover:scale-110 hover:-translate-y-1"
                  title="YouTube"
                >
                  <i class="fab fa-youtube text-white text-lg"></i>
                </a>
              </div>
            </div>

            <!-- Service Times Quick Info -->
            <div
              class="bg-white/5 backdrop-blur-sm rounded-lg p-4 border border-white/10"
            >
              <p class="text-white text-sm mb-2 font-semibold">
                Service Times
              </p>
              <div class="space-y-1 text-xs text-white">
                <p>
                  <span class="text-blue-300">Sunday:</span> 9:30 AM - 12:00 PM
                </p>
                <p>
                  <span class="text-blue-300">Friday:</span> 5:00 PM - 6:00 PM
                </p>
                <p>
                  <span class="text-blue-300">Wednesday:</span> 5:30 PM - 6:30
                  PM
                </p>
              </div>
            </div>
          </div>
        </div>

        <!-- Divider with Cross -->
        <div class="flex items-center justify-center mb-8">
          <div class="flex-1 border-t border-amber-700/50"></div>
          <div
            class="bg-gradient-to-br from-blue-500 to-blue-600 w-12 h-12 rounded-full flex items-center justify-center mx-6 shadow-lg overflow-hidden"
          >
            <img
              :src="founderImageUrl"
              alt="Jesus Solution Ministry Logo"
              class="w-8 h-8 object-contain"
            />
          </div>
          <div class="flex-1 border-t border-amber-700/50"></div>
        </div>

        <!-- Bottom Section -->
        <div class="text-center">
          <div class="mb-4">
            <p class="text-white text-sm italic mb-2">
             Jesus said, "Come to Me; All you who are weary and burdened, And I will Give You Rest"
            </p>
            <p class="text-white text-xs font-semibold">- Matthew 11:23</p>
          </div>

          <div class="border-t border-amber-700/30 pt-6">
            <p class="text-amber-100 text-sm">
              &copy; 2025
              <span class="font-semibold text-white"
                >Jesus Christ Solution Ministry</span
              >. All rights reserved.
            </p>
            <p class="text-white text-xs mt-1">
              Built with love and faith for God's glory
            </p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script lang="ts" setup>
import founderImageUrl from "../../assets/logo.png";

// Scroll to section functionality
const scrollToSection = (sectionId: string) => {
  const element = document.getElementById(sectionId);
  if (element) {
    element.scrollIntoView({ behavior: "smooth" });
  }
};

// Contact actions
const callPhone = () => {
  window.open("tel:0792665651", "_self");
};

const sendEmail = () => {
  window.open("mailto:info@jcsministry.org", "_self");
};
</script>

<style scoped>
/* Enhanced gradient animations */
.bg-gradient-to-b {
  background-size: 100% 200%;
  animation: gradientShift 8s ease-in-out infinite;
}

@keyframes gradientShift {
  0%,
  100% {
    background-position: 0% 0%;
  }
  50% {
    background-position: 0% 100%;
  }
}

/* Icon hover effects */
.rounded-full:hover {
  transform: rotate(360deg) scale(1.1);
  transition: transform 0.5s ease;
}

.rounded-lg:hover {
  transform: scale(1.05);
  transition: transform 0.3s ease;
}

/* Link hover effects */
a:hover .w-2 {
  animation: pulse 1s infinite;
}

@keyframes pulse {
  0%,
  100% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(1.5);
    opacity: 0.7;
  }
}

/* Backdrop blur support */
.backdrop-blur-sm {
  backdrop-filter: blur(4px);
}

/* Social media hover animations */
.fab:hover {
  animation: socialBounce 0.6s ease;
}

@keyframes socialBounce {
  0%,
  20%,
  50%,
  80%,
  100% {
    transform: translateY(0);
  }
  40% {
    transform: translateY(-8px);
  }
  60% {
    transform: translateY(-4px);
  }
}

/* Enhanced text shadows for better readability */
h3,
.font-bold {
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
}

/* Smooth transitions for all interactive elements */
* {
  transition: all 0.3s ease;
}

/* Mobile responsiveness */
@media (max-width: 768px) {
  .grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .md\:col-span-1 {
    text-align: center;
  }

  .flex {
    justify-content: center;
  }

  .space-x-3 > * + * {
    margin-left: 0.75rem;
  }
}

/* Focus states for accessibility */
a:focus,
button:focus {
  outline: 2px solid #60a5fa;
  outline-offset: 2px;
  border-radius: 4px;
}

/* Loading states */
.loading {
  animation: shimmer 1.5s infinite;
}

@keyframes shimmer {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
  }
}
</style>
