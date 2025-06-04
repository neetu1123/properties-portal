<template>
    <div class="py-16">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <p class="lightText text-sm font-medium mb-2 uppercase tracking-wider">what our guests say</p>
                <h2 class="text-4xl font-bold text-gray-900 mb-4">
                    Guest <span class="lightText">Reviews</span>
                </h2>
                <p class="text-gray-600 max-w-2xl mx-auto">
                    Get inspired by glowing guest reviews that showcase the exceptional experiences and
                    unforgettable memories created by the staff at Special Places of Costa Rica.
                </p>
            </div>
            <div class="relative mb-16">
                <div
                    class="bg-gradient-to-r from-[#4a8a9e] to-[#5ea8bd] transform rounded-3xl p-60 max-w-5xl mx-auto relative overflow-hidden shadow-2xl">
                    <!-- Subtle pattern overlay -->
                    <div class="absolute inset-0 opacity-10"
                        style="background-image: url('data:image/svg+xml,%3Csvg width=\'20\' height=\'20\' viewBox=\'0 0 20 20\' xmlns=\'http://www.w3.org/2000/svg\'%3E%3Cg fill=\'%23ffffff\' fill-opacity=\'1\' fill-rule=\'evenodd\'%3E%3Ccircle cx=\'3\' cy=\'3\' r=\'3\'/%3E%3Ccircle cx=\'13\' cy=\'13\' r=\'3\'/%3E%3C/g%3E%3C/svg%3E');">
                    </div>
                </div>

                <!-- Slider container -->
                <div ref="sliderRef"
                    class="review-slider absolute top-14 flex overflow-x-hidden gap-8 pb-8 scrollbar-hide px-6 md:px-10">
                    <!-- Review Card 1 -->
                    <div
                        class="review-card relative bg-white p-6 rounded-xl shadow-xl transform transition-all duration-300 hover:scale-105 z-10 border border-gray-100">
                        <div
                            class="absolute -top-5 -left-5 bg-gradient-to-r from-blue-500 to-blue-600 text-white w-14 h-14 rounded-full flex items-center justify-center shadow-lg">
                            <Icon name="mdi:account" width="28" height="28" />
                        </div>
                        <div class="ml-8 mb-4 border-b border-gray-100 pb-3">
                            <h3 class="text-xl font-bold text-gray-800">Ethan Parker</h3>
                            <div class="flex items-center justify-between">
                                <p class="text-gray-500 text-sm">Guest</p>
                               
                            </div>
                        </div>
                        <div class="relative">
                            <Icon name="mdi:format-quote-open" width="24" height="24"
                                class="text-gray-200 absolute -top-2 -left-1" />
                            <p class="text-gray-700 mb-3 pt-3 italic text-sm md:text-base pl-6">La Casa Raja e molto
                                bella e comoda. Noi cavamo in 6 con
                                un cagnolino e siamo stati benissimo. Molto pulita e spaziosa. Tutt' gli ambienti sono
                                comodi e piacevoli...</p>
                            <Icon name="mdi:format-quote-close" width="24" height="24"
                                class="text-gray-200 absolute bottom-0 right-0" />
                        </div>
                        <div class="mt-4 pt-3 border-t border-gray-100 flex justify-end">
                            <div class="flex text-yellow-400">
                                    <Icon v-for="i in 5" :key="i" name="mdi:star" width="16" height="16" class="ml-1" />
                                </div>
                        </div>
                    </div>

                    <!-- Review Card 2 -->
                    <div
                        class="review-card relative bg-white p-6 rounded-xl shadow-xl transform transition-all duration-300 hover:scale-105 z-10 border border-gray-100">
                        <div
                            class="absolute -top-5 -left-5 bg-gradient-to-r from-pink-500 to-pink-600 text-white w-14 h-14 rounded-full flex items-center justify-center shadow-lg">
                            <Icon name="mdi:account" width="28" height="28" />
                        </div>
                        <div class="ml-8 mb-4 border-b border-gray-100 pb-3">
                            <h3 class="text-xl font-bold text-gray-800">Ava Thompson</h3>
                            <div class="flex items-center justify-between">
                                <p class="text-gray-500 text-sm">Guest</p>
                               
                            </div>
                        </div>
                        <div class="relative">
                            <Icon name="mdi:format-quote-open" width="24" height="24"
                                class="text-gray-200 absolute -top-2 -left-1" />
                            <p class="text-gray-700 mb-3 pt-3 italic text-sm md:text-base pl-6">Nosebbe lugar ! Una
                                vista espectacular definitivamente en
                                el paraíso, muy confortable y muy amables y seguro y mucha privacidad súper recomendado
                                perfecta ubicación cerca de muchas playas...</p>
                            <Icon name="mdi:format-quote-close" width="24" height="24"
                                class="text-gray-200 absolute bottom-0 right-0" />
                        </div>
                        <div class="mt-4 pt-3 border-t border-gray-100 flex justify-end">
                           <div class="flex text-yellow-400">
                                    <Icon v-for="i in 5" :key="i" name="mdi:star" width="16" height="16" class="ml-1" />
                                </div>
                        </div>
                    </div>

                    <!-- Review Card 3 -->
                    <div
                        class="review-card relative bg-white p-6 rounded-xl shadow-xl transform transition-all duration-300 hover:scale-105 z-10 border border-gray-100">
                        <div
                            class="absolute -top-5 -left-5 bg-gradient-to-r from-purple-500 to-purple-600 text-white w-14 h-14 rounded-full flex items-center justify-center shadow-lg">
                            <Icon name="mdi:account" width="28" height="28" />
                        </div>
                        <div class="ml-8 mb-4 border-b border-gray-100 pb-3">
                            <h3 class="text-xl font-bold text-gray-800">Olivia Williams</h3>
                            <div class="flex items-center justify-between">
                                <p class="text-gray-500 text-sm">Guest</p>
                               
                            </div>
                        </div>
                        <div class="relative">
                            <Icon name="mdi:format-quote-open" width="24" height="24"
                                class="text-gray-200 absolute -top-2 -left-1" />
                            <p class="text-gray-700 mb-3 pt-3 italic text-sm md:text-base pl-6">Very nice condo! Special
                                places arranged for the transfer
                                from the airport and everything went very smoothly. The condo was large and beautiful,
                                and
                                the third floor allowed for a lovely view...</p>
                            <Icon name="mdi:format-quote-close" width="24" height="24"
                                class="text-gray-200 absolute bottom-0 right-0" />
                        </div>
                        <div class="mt-4 pt-3 border-t border-gray-100 flex justify-end">
                             <div class="flex text-yellow-400">
                                    <Icon v-for="i in 5" :key="i" name="mdi:star" width="16" height="16" class="ml-1" />
                                </div>
                        </div>
                    </div>
                     <!-- Review Card 3 -->
                    <div
                        class="review-card relative bg-white p-6 rounded-xl shadow-xl transform transition-all duration-300 hover:scale-105 z-10 border border-gray-100">
                        <div
                            class="absolute -top-5 -left-5 bg-gradient-to-r from-purple-500 to-purple-600 text-white w-14 h-14 rounded-full flex items-center justify-center shadow-lg">
                            <Icon name="mdi:account" width="28" height="28" />
                        </div>
                        <div class="ml-8 mb-4 border-b border-gray-100 pb-3">
                            <h3 class="text-xl font-bold text-gray-800">Olivia Williams</h3>
                            <div class="flex items-center justify-between">
                                <p class="text-gray-500 text-sm">Guest</p>
                             
                            </div>
                        </div>
                        <div class="relative">
                            <Icon name="mdi:format-quote-open" width="24" height="24"
                                class="text-gray-200 absolute -top-2 -left-1" />
                            <p class="text-gray-700 mb-3 pt-3 italic text-sm md:text-base pl-6">Very nice condo! Special
                                places arranged for the transfer
                                from the airport and everything went very smoothly. The condo was large and beautiful,
                                and
                                the third floor allowed for a lovely view...</p>
                            <Icon name="mdi:format-quote-close" width="24" height="24"
                                class="text-gray-200 absolute bottom-0 right-0" />
                        </div>
                        <div class="mt-4 pt-3 border-t border-gray-100 flex justify-end">
                            <div class="flex text-yellow-400">
                                    <Icon v-for="i in 5" :key="i" name="mdi:star" width="16" height="16" class="ml-1" />
                                </div>
                        </div>
                    </div>
                </div>

                <!-- Navigation arrows -->
                <button @click="goToPrev"
                    class="absolute left-2 top-1/2 -translate-y-1/2 bg-white p-3 rounded-full shadow-xl hover:bg-gray-50 hover:scale-110 transition-all duration-300 z-20 focus:outline-none focus:ring-2 focus:ring-blue-300 hidden md:flex items-center justify-center">
                    <Icon name="mdi:chevron-left" width="24" height="24" class="text-gray-700" />
                </button>
                <button @click="goToNext"
                    class="absolute right-2 top-1/2 -translate-y-1/2 bg-white p-3 rounded-full shadow-xl hover:bg-gray-50 hover:scale-110 transition-all duration-300 z-20 focus:outline-none focus:ring-2 focus:ring-blue-300 hidden md:flex items-center justify-center">
                    <Icon name="mdi:chevron-right" width="24" height="24" class="text-gray-700" />
                </button>

                <!-- Navigation dots (mobile friendly) -->
                <div class="absolute bottom-4 left-0 right-0 flex justify-center space-x-2">
                    <button v-for="(_, index) in 3" :key="index" @click="goToSlide(index)"
                        class="w-3 h-3 rounded-full transition-colors duration-200 focus:outline-none"
                        :class="currentIndex === index ? 'bg-[#4a8a9e]' : 'bg-gray-300'"></button>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'

const sliderRef = ref<HTMLElement | null>(null)
const currentIndex = ref(0)

function updateSlider() {
    if (!sliderRef.value) return

    const slider = sliderRef.value
    const cards = slider.querySelectorAll('.review-card')
    if (!cards.length) return

    const cardWidth = (cards[0] as HTMLElement).offsetWidth + 32 // width + gap
    slider.scrollTo({
        left: currentIndex.value * cardWidth,
        behavior: 'smooth'
    })
}

function goToSlide(index: number) {
    if (index >= 0 && index <= 2) { // Assuming 3 cards
        currentIndex.value = index
        updateSlider()
    }
}

function goToNext() {
    if (!sliderRef.value) return

    const cards = sliderRef.value.querySelectorAll('.review-card')
    if (currentIndex.value < cards.length - 1) {
        currentIndex.value++
        updateSlider()
    }
}

function goToPrev() {
    if (currentIndex.value > 0) {
        currentIndex.value--
        updateSlider()
    }
}

onMounted(() => {
    // Make sure references are properly set after component is mounted
    updateSlider()
})
</script>

<style scoped>
.review-slider {
    scroll-snap-type: x mandatory;
    -ms-overflow-style: none;
    scrollbar-width: none;
}

.review-slider::-webkit-scrollbar {
    display: none;
}

.review-card {
    scroll-snap-align: start;
    flex: 0 0 85%;
    max-width: 350px;
}

@media (min-width: 768px) {
    .review-card {
        flex: 0 0 40%;
        max-width: 380px;
    }
}

.lightText {
    color: #4a8a9e;
}

/* Add subtle animation for the quote marks */
@keyframes float {
    0% {
        transform: translateY(0px);
    }

    50% {
        transform: translateY(-3px);
    }

    100% {
        transform: translateY(0px);
    }
}

.text-gray-200.absolute {
    opacity: 0.5;
    animation: float 3s ease-in-out infinite;
}
</style>