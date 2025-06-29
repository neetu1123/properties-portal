<template>
    <div class="mt-28 min-h-screen py-8">
        <div class="container mx-auto px-4 max-w-4xl">
            <!-- Header Section -->
            <div class="text-center mb-12">
                <p class="text-sm font-semibold text-gray-600 uppercase tracking-wider mb-4">FAQS</p>
                <h1 class="text-3xl md:text-4xl lg:text-5xl font-serif text-navy mb-6">
                    Frequently Asked Questions
                </h1>
                <p class="text-gray-600 max-w-2xl mx-auto leading-relaxed">
                    Our frequently asked questions may also be of assistance. Nevertheless, don't hesitate to give us a
                    call
                    <span class="font-semibold text-navy">(912) 499-0777</span>. We'll be happy to have a South Key
                    representative answer any additional questions before you get here or during your stay.
                </p>
            </div>

            <!-- FAQ Accordion -->
            <div class="space-y-4">
                <!-- FAQ Item -->
                <div v-for="(faq, index) in faqs" :key="index" class="bg-white rounded-lg border border-gold shadow-sm">
                    <button
                        class="w-full px-6 py-5 text-left flex items-center justify-between hover:bg-gray-50 transition-colors duration-200 focus:outline-none focus:ring-2 focus:ring-gold focus:ring-opacity-50"
                        @click="toggleFAQ(index)">
                        <div class="flex items-center gap-4">
                            <Icon name="mdi:star-four-points" class="text-gold text-xl flex-shrink-0" />
                            <span class="text-navy font-medium text-lg">{{ faq.question }}</span>
                        </div>
                        <Icon :name="activeIndex === index ? 'mdi:close' : 'mdi:plus'"
                            class="text-navy text-2xl transition-transform duration-700 flex-shrink-0"
                            :class="{ 'rotate-45': activeIndex === index }" />
                    </button>
                    <div class="overflow-hidden transition-all duration-300 ease-in-out"
                        :class="{ 'max-h-0': activeIndex !== index, 'max-h-96': activeIndex === index }">
                        <div class="px-6 pb-5 pt-0">
                            <div class="pl-10">
                                <p class="text-gray-600 leading-relaxed">
                                    {{ faq.answer }}
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const activeIndex = ref(null);

const toggleFAQ = (index) => {
    activeIndex.value = activeIndex.value === index ? null : index;
};

const faqs = [
    {
        question: "May I check-in early or check-out late?",
        answer: "Early check-in and late check-out are subject to availability. Please contact us in advance to arrange these services. Additional fees may apply for late check-out requests."
    },
    {
        question: "What is your policy on pets?",
        answer: "We welcome well-behaved pets in designated pet-friendly accommodations. A pet fee applies, and advance notice is required. Please review our complete pet policy for specific guidelines and restrictions."
    },
    {
        question: "Do you offer baby equipment?",
        answer: "Yes, we provide various baby equipment including cribs, high chairs, and baby gates upon request. Please let us know your needs when making your reservation to ensure availability."
    },
    {
        question: "Where will I park?",
        answer: "Complimentary parking is available on-site for all guests. Specific parking assignments will be provided upon check-in. Additional parking options are available for guests with multiple vehicles."
    },
    {
        question: "Do you have cooking utensils?",
        answer: "All our accommodations with kitchens come fully equipped with cooking utensils, cookware, dishes, and basic appliances. A complete inventory list is available upon request."
    },
    {
        question: "Do you provide coffee?",
        answer: "Yes, complimentary coffee and tea are provided in all accommodations. Coffee makers and a starter supply of coffee, tea, and filters are included."
    },
    {
        question: "Can we leave our bags in the apartment before check-in?",
        answer: "Luggage storage is available at the front desk for early arrivals. For security reasons, bags cannot be left in apartments before check-in, but our staff will be happy to securely store them for you."
    },
    {
        question: "Do you provide linens/towels?",
        answer: "Yes, all linens and towels are provided including bed sheets, pillowcases, blankets, bath towels, hand towels, and washcloths. Fresh linens are provided for extended stays."
    }
];
</script>

<style scoped>
.text-navy {
    color: #2C3E50;
}

.text-gold {
    color: #D4AF37;
}

.border-gold {
    border-color: #D4AF37;
}

.ring-gold {
    --tw-ring-color: #D4AF37;
}
</style>