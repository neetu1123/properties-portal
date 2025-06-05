<template>
  <div class="bg-white">
    <div class="mx-auto max-w-7xl px-6 py-16 sm:py-24">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-4xl lg:text-5xl font-bold text-gray-900">Frequently asked questions</h2>
      </div>
      <div class="mt-20">
        <dl class="space-y-16 sm:grid sm:grid-cols-2 sm:gap-x-6 sm:gap-y-16 sm:space-y-0 lg:gap-x-10">
          <div v-for="faq in faqs" :key="faq.id">
            <dt class="text-base font-semibold leading-7 text-gray-900">{{ faq.question }}</dt>
            <dd class="mt-2 text-base leading-7 text-gray-600">{{ faq.answer }}</dd>
          </div>
        </dl>
      </div>
      <div class="flex justify-center mt-8">

        <button
          class="bgGradient text-white px-8 py-3 rounded-lg font-semibold transition-colors inline-flex items-center">
         Show All
          <Icon name="lucide:arrow-right" width="20" height="20" class="!size-5 ml-2" />
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
const faqs = [
  {
    id: 1,
    question: "How close is the property to the beach?",
    answer:
      "Our home is just a short walk or bike ride from the beautiful white sands of Inlet Beach—perfect for morning strolls or sunset views.",
  },
  {
    id: 1,
    question: "What amenities are included in the rental?",
    answer:
      "You’ll enjoy a fully equipped kitchen, high-speed Wi-Fi, smart TVs, a washer/dryer, outdoor seating, and complimentary beach gear. Some properties may also include a private pool or hot tub.",
  },
  {
    id: 1,
    question: "Are there restaurants and shops nearby?",
    answer:
      "Yes! You’re minutes away from 30Avenue, Rosemary Beach, and other nearby dining, shopping, and entertainment options.",
  },
  {
    id: 1,
    question: " Is the property family-friendly?",
    answer:
      "Absolutely! We welcome families and provide family-friendly features like board games, bunk beds (in some units), and safe outdoor spaces.",
  },
  {
    id: 1,
    question: "Do you allow pets?",
    answer:
      "Some of our homes are pet-friendly with prior approval and a pet fee. Please contact us with details about your pet before booking.",
  },
  {
    id: 1,
    question: "What is your cancellation policy?",
    answer:
      "We offer a flexible cancellation policy depending on the season and listing platform. Please check your reservation details or contact us directly for the most accurate info.",
  },
  // More questions...
]
</script>