<template>
  <section
    id="offering"
    class="py-20 bg-gradient-to-b from-blue-800 to-blue-900"
  >
    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Enhanced Title Section -->
      <div class="text-center mb-16 animate-fade-in-up" ref="offeringTitle">
        <div class="inline-block">
          <h2 class="text-4xl md:text-5xl font-bold text-amber-900 mb-4">
            Online Giving
          </h2>
          <div
            class="w-24 h-1 bg-gradient-to-r from-transparent via-amber-500 to-transparent mx-auto mb-6"
          ></div>
        </div>
        <p class="text-lg text-white/90 font-light">
          Support our ministry through secure digital offerings
        </p>
      </div>

      <!-- Enhanced M-Pesa Offering Section -->
      <div
        class="bg-white/95 backdrop-blur-sm rounded-2xl shadow-2xl overflow-hidden animate-fade-in-up animation-delay-300 border border-white/20"
        ref="offeringCard"
      >
        <!-- M-Pesa Header -->
        <div
          class="bg-gradient-to-r from-green-600 to-green-500 p-8 text-center"
        >
          <div
            class="inline-flex items-center justify-center w-20 h-20 bg-white/20 backdrop-blur-sm rounded-full mb-6 shadow-lg"
          >
            <span class="text-white font-bold text-3xl">M</span>
          </div>
          <h3 class="text-3xl font-bold text-white mb-2">LIPA NA M-Pesa</h3>
          <p class="text-white/90 text-lg font-light">
            Secure, fast, and convenient mobile payments
          </p>
        </div>

        <!-- Payment Details Section -->
        <div class="p-8 md:p-12">
          <!-- Service Provider Info -->
          <div class="mb-8">
            <div class="flex items-center mb-6">
              <div
                class="bg-gradient-to-br from-blue-500 to-blue-600 w-12 h-12 rounded-full flex items-center justify-center mr-4 shadow-lg"
              >
                <i class="fas fa-university text-white text-lg"></i>
              </div>
              <h4 class="text-2xl font-bold text-amber-900">SKYLINE SACCO</h4>
            </div>

            <!-- Payment Details Grid -->
            <div
              class="bg-blue-50/50 backdrop-blur-sm rounded-xl p-6 space-y-4 border border-blue-100"
            >
              <div
                class="flex flex-col sm:flex-row sm:justify-between sm:items-center p-4 bg-white/60 rounded-lg"
              >
                <span class="text-gray-700 font-medium mb-2 sm:mb-0"
                  >Paybill Number:</span
                >
                <div class="flex items-center">
                  <span class="font-bold text-2xl text-blue-800 mr-3"
                    >116519</span
                  >
                  <button
                    class="text-blue-600 hover:text-blue-800 transition-colors"
                    @click="copyToClipboard('116519')"
                    title="Copy to clipboard"
                  >
                    <i class="fas fa-copy"></i>
                  </button>
                </div>
              </div>

              <div
                class="flex flex-col sm:flex-row sm:justify-between sm:items-center p-4 bg-white/60 rounded-lg"
              >
                <span class="text-gray-700 font-medium mb-2 sm:mb-0"
                  >Account Number:</span
                >
                <div class="flex items-center">
                  <span class="font-bold text-2xl text-amber-800 mr-3"
                    >007011</span
                  >
                  <button
                    class="text-amber-600 hover:text-amber-800 transition-colors"
                    @click="copyToClipboard('007011')"
                    title="Copy to clipboard"
                  >
                    <i class="fas fa-copy"></i>
                  </button>
                </div>
              </div>

              <div
                class="flex flex-col sm:flex-row sm:justify-between sm:items-center p-4 bg-white/60 rounded-lg"
              >
                <span class="text-gray-700 font-medium mb-2 sm:mb-0"
                  >Account Name:</span
                >
                <span class="font-bold text-lg text-gray-900"
                  >JESUS SOLUTION MINISTRY</span
                >
              </div>
            </div>
          </div>

          <!-- How to Pay Instructions -->
          <div
            class="bg-gradient-to-br from-amber-50 to-amber-100/50 rounded-xl p-6 border-l-4 border-amber-500"
          >
            <h5 class="text-lg font-bold text-amber-900 mb-4 flex items-center">
              <i class="fas fa-mobile-alt text-amber-600 mr-2"></i>
              How to Send Your Offering
            </h5>
            <div class="space-y-3 text-gray-700">
              <div class="flex items-start">
                <span
                  class="bg-amber-500 text-white w-6 h-6 rounded-full flex items-center justify-center text-sm font-bold mr-3 mt-0.5"
                  >1</span
                >
                <span>Go to M-Pesa on your phone</span>
              </div>
              <div class="flex items-start">
                <span
                  class="bg-amber-500 text-white w-6 h-6 rounded-full flex items-center justify-center text-sm font-bold mr-3 mt-0.5"
                  >2</span
                >
                <span>Select "Lipa na M-Pesa" then "Pay Bill"</span>
              </div>
              <div class="flex items-start">
                <span
                  class="bg-amber-500 text-white w-6 h-6 rounded-full flex items-center justify-center text-sm font-bold mr-3 mt-0.5"
                  >3</span
                >
                <span>Enter Business Number: <strong>116519</strong></span>
              </div>
              <div class="flex items-start">
                <span
                  class="bg-amber-500 text-white w-6 h-6 rounded-full flex items-center justify-center text-sm font-bold mr-3 mt-0.5"
                  >4</span
                >
                <span>Enter Account Number: <strong>007011</strong></span>
              </div>
              <div class="flex items-start">
                <span
                  class="bg-amber-500 text-white w-6 h-6 rounded-full flex items-center justify-center text-sm font-bold mr-3 mt-0.5"
                  >5</span
                >
                <span>Enter your offering amount and PIN</span>
              </div>
            </div>
          </div>

          <!-- Gratitude Message -->
          <div
            class="text-center mt-8 p-6 bg-blue-50/50 rounded-xl border border-blue-100"
          >
            <div
              class="bg-gradient-to-br from-blue-500 to-blue-600 w-12 h-12 rounded-full flex items-center justify-center mx-auto mb-4 shadow-lg"
            >
              <i class="fas fa-heart text-white text-lg"></i>
            </div>
            <p class="text-gray-700 font-medium italic">
              "Thank you for your generous heart and faithful stewardship. Your
              offerings help us continue God's work in our community."
            </p>
            <p class="text-blue-800 font-semibold mt-2">
              - Jesus Solution Ministry Team
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref, onMounted } from "vue";

// Template refs
const offeringTitle = ref(null);
const offeringCard = ref(null);

// Copy to clipboard function
const copyToClipboard = async (text: string) => {
  try {
    await navigator.clipboard.writeText(text);
    // You can add a toast notification here
    console.log(`Copied to clipboard: ${text}`);
  } catch (err) {
    console.error("Failed to copy: ", err);
    // Fallback for older browsers
    const textArea = document.createElement("textarea");
    textArea.value = text;
    document.body.appendChild(textArea);
    textArea.select();
    document.execCommand("copy");
    document.body.removeChild(textArea);
  }
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
  const elements = [offeringTitle.value, offeringCard.value];

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

/* Intersection observer visible state */
.animate-visible {
  opacity: 1;
  transform: translateY(0);
}

/* Enhanced card hover effects */
.bg-white\/95:hover {
  transform: translateY(-4px);
  box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
  transition: all 0.4s ease;
}

/* Backdrop blur support */
.backdrop-blur-sm {
  backdrop-filter: blur(4px);
}

/* Enhanced shadow effects */
.shadow-2xl {
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
}

/* Copy button hover effects */
button:hover {
  transform: scale(1.1);
  transition: transform 0.2s ease;
}

/* Icon container hover effects */
.rounded-full:hover {
  transform: rotate(5deg) scale(1.05);
  transition: transform 0.3s ease;
}

/* Gradient animations */
.bg-gradient-to-r {
  background-size: 200% 200%;
  animation: gradient 3s ease infinite;
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

/* Step number animations */
.bg-amber-500 {
  transition: all 0.3s ease;
}

.bg-amber-500:hover {
  transform: scale(1.1) rotate(360deg);
  box-shadow: 0 4px 12px rgba(245, 158, 11, 0.4);
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .p-8 {
    padding: 1.5rem;
  }

  .md\:p-12 {
    padding: 2rem;
  }

  .text-4xl {
    font-size: 2rem;
  }

  .text-3xl {
    font-size: 1.75rem;
  }

  .text-2xl {
    font-size: 1.25rem;
  }

  .flex-col {
    gap: 0.5rem;
  }
}

/* Enhanced focus states for accessibility */
button:focus {
  outline: 2px solid #3b82f6;
  outline-offset: 2px;
}

/* Smooth transitions for all interactive elements */
* {
  transition: color 0.2s ease, background-color 0.2s ease, transform 0.2s ease;
}
</style>
