<template>
  <!-- Main Content -->
  <section id="offering" class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
    <!-- M-Pesa Offering Section -->
    <div class="bg-amber-900 rounded-2xl shadow-lg p-8 md:p-12">
      <!-- M-Pesa Logo and Title -->
      <div class="text-center mb-12">
        <div
          class="inline-flex items-center justify-center w-20 h-20 bg-green-600 rounded-full mb-6"
        >
          <span class="text-white font-bold text-2xl">M</span>
        </div>
        <h1 class="text-3xl font-bold text-white mb-2">LIPA NA M-Pesa</h1>
        <p class="text-white text-lg">
          Secure, fast, and convenient mobile payments
        </p>
      </div>

      <!-- M-Pesa Payment Details -->
      <div class="bg-gray-50 rounded-xl p-6 mb-8">
        <h3 class="text-lg font-semibold text-gray-900 mb-4 flex items-center">
          <i class="fas fa-info-circle text-blue-500 mr-2"></i>
          SKYLINE SACCO
        </h3>
        <div class="grid grid-cols-1 gap-4">
          <div class="flex justify-between items-center">
            <span class="text-gray-900">Paybill Number:</span>
            <span class="font-semibold text-gray-900">116519</span>
          </div>
          <div class="flex justify-between items-center">
            <span class="text-gray-900">Account Number:</span>
            <span class="font-semibold text-gray-900">007011</span>
          </div>
          <div class="flex justify-between items-center">
            <span class="text-gray-900">Account Name:</span>
            <span class="font-semibold text-gray-900"
              >JESUS SOLUTION MINISTRY</span
            >
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref } from "vue";

// Reactive data for form inputs
const paymentAmount = ref("");
const phoneNumber = ref("");

// Handle payment button click
const handlePayment = () => {
  if (!paymentAmount.value || !phoneNumber.value) {
    alert("Please enter both amount and phone number");
    return;
  }

  // Add your M-Pesa payment logic here
  console.log("Processing M-Pesa payment...", {
    amount: paymentAmount.value,
    phone: phoneNumber.value,
  });

  // You can emit events, call APIs, or handle payment processing
  // Example: initiate M-Pesa STK push or redirect to payment gateway
};
</script>

<style scoped>
/* Ensure Font Awesome icons are properly displayed */
.fas {
  display: inline-block;
  font-family: "Font Awesome 5 Free";
  font-weight: 900;
}

/* Custom button styling */
button {
  border-radius: 8px;
}

/* Input focus styles */
input:focus {
  outline: none;
}
</style>
