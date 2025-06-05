<template>
    <div class="py-16">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <p class="lightText text-sm font-medium mb-2 uppercase tracking-wider">what our guests say</p>
                <h2 class="text-4xl font-bold text-gray-900 mb-4">
                    Guest <span class="lightText">Reviews</span>
                </h2>

            </div>
            <div class="relative mb-16">
                <div
                    class="bg-gradient-to-r from-[#4a8a9e] to-[#5ea8bd] transform rounded-4xl px-24 py-64 max-w-4xl mx-auto relative overflow-hidden shadow-2xl">
                    <!-- Subtle pattern overlay -->
                    <div class="absolute inset-0 opacity-10"
                        style="background-image: url('data:image/svg+xml,%3Csvg width=\'20\' height=\'20\' viewBox=\'0 0 20 20\' xmlns=\'http://www.w3.org/2000/svg\'%3E%3Cg fill=\'%23ffffff\' fill-opacity=\'1\' fill-rule=\'evenodd\'%3E%3Ccircle cx=\'3\' cy=\'3\' r=\'3\'/%3E%3Ccircle cx=\'13\' cy=\'13\' r=\'3\'/%3E%3C/g%3E%3C/svg%3E');">
                    </div>
                </div>

                <!-- Slider container -->
                <div ref="sliderRef"
                    class="review-slider absolute top-24 flex overflow-x-hidden gap-8 pb-8 px-6 md:px-10 z-10">
                    <!-- Review Card 1 -->
                    <div
                        class="review-card relative bg-white p-6 rounded-lg shadow-xl transition-transform duration-500 hover:rounded-none hover:scale-110 border border-gray-100">
                        <!-- <div
                            class="absolute -top-0 -left-5 bg-gradient-to-r from-blue-500 to-blue-600 text-white w-14 h-14 rounded-full flex items-center justify-center shadow-lg">
                            <Icon name="lucide:user" class="!size-6" width="28" height="28" />
                        </div> -->
                        <div class="mx-8 mb-4 border-b border-gray-100 pb-3">
                            <h3 class="text-xl font-bold text-gray-800">Ethan Parker</h3>
                            <div class="flex items-center justify-between">
                                <p class="text-gray-500 text-sm">Guest</p>

                            </div>
                        </div>
                        <div class="relative">
                            <!-- <Icon name="lucide:quote" width="24" height="24"
                                class="text-gray-200 absolute -top-2 -left-1" /> -->
                            <p class="text-gray-700 mb-3 pt-3 italic text-sm md:text-base pl-6">La Casa Raja e molto
                                bella e comoda. Noi cavamo in 6 con
                                un cagnolino e siamo stati benissimo. Molto pulita e spaziosa. Tutt' gli ambienti sono
                                comodi e piacevoli...</p>
                            <Icon name="lucide:format-quote-close" width="24" height="24"
                                class="text-gray-200 absolute bottom-0 right-0" />
                        </div>
                        <div class="mt-4 pt-3 border-t border-gray-100 flex justify-end">
                            <div class="flex text-yellow-400">
                                <Icon v-for="i in 5" :key="i" name="lucide:star" width="16" height="16" class="ml-1" />
                            </div>
                        </div>
                    </div>

                    <!-- Review Card 2 -->
                    <div
                        class="review-card relative bg-white p-6 rounded-lg shadow-xl transition-transform duration-500 hover:rounded-none hover:scale-110 border border-gray-100">
                        <!-- <div
                            class="absolute -top-1 -left-4 bg-gradient-to-r from-pink-500 to-pink-600 text-white w-14 h-14 rounded-full flex items-center justify-center shadow-lg">
                            <Icon name="lucide:user" class="!size-6" width="28" height="28" />
                        </div> -->
                        <div class="mx-8 mb-4 border-b border-gray-100 pb-3">
                            <h3 class="text-xl font-bold text-gray-800">Ava Thompson</h3>
                            <div class="flex items-center justify-between">
                                <p class="text-gray-500 text-sm">Guest</p>

                            </div>
                        </div>
                        <div class="relative">
                            <Icon name="lucide:quote" width="24" height="24"
                                class="text-gray-200 absolute -top-2 -left-1" />
                            <p class="text-gray-700 mb-3 pt-3 italic text-sm md:text-base pl-6">Nosebbe lugar ! Una
                                vista espectacular definitivamente en
                                el paraíso, muy confortable y muy amables y seguro y mucha privacidad súper recomendado
                                perfecta ubicación cerca de muchas playas...</p>
                            <Icon name="lucide:format-quote-close" width="24" height="24"
                                class="text-gray-200 absolute bottom-0 right-0" />
                        </div>
                        <div class="mt-4 pt-3 border-t border-gray-100 flex justify-end">
                            <div class="flex text-yellow-400">
                                <Icon v-for="i in 5" :key="i" name="lucide:star" width="16" height="16" class="ml-1" />
                            </div>
                        </div>
                    </div>

                    <!-- Review Card 3 -->
                    <div
                        class="review-card relative bg-white p-6 rounded-lg shadow-xl transition-transform duration-500 hover:rounded-none hover:scale-110 border border-gray-100">
                        <!-- <div
                            class="absolute -top-0 -left-5  bg-gradient-to-r from-purple-500 to-purple-600 text-white w-14 h-14 rounded-full flex items-center justify-center shadow-lg">
                            <Icon name="lucide:user" class="!size-6" width="28" height="28" />
                        </div> -->
                        <div class="mx-8 mb-4 border-b border-gray-100 pb-3">
                            <h3 class="text-xl font-bold text-gray-800">Olivia Williams</h3>
                            <div class="flex items-center justify-between">
                                <p class="text-gray-500 text-sm">Guest</p>

                            </div>
                        </div>
                        <div class="relative">
                            <Icon name="lucide:quote" width="24" height="24"
                                class="text-gray-200 absolute -top-2 -left-1" />
                            <p class="text-gray-700 mb-3 pt-3 italic text-sm md:text-base pl-6">Very nice condo! Special
                                places arranged for the transfer
                                from the airport and everything went very smoothly. The condo was large and beautiful,
                                and
                                the third floor allowed for a lovely view...</p>
                            <Icon name="lucide:format-quote-close" width="24" height="24"
                                class="text-gray-200 absolute bottom-0 right-0" />
                        </div>
                        <div class="mt-4 pt-3 border-t border-gray-100 flex justify-end">
                            <div class="flex text-yellow-400">
                                <Icon v-for="i in 5" :key="i" name="lucide:star" width="16" height="16" class="ml-1" />
                            </div>
                        </div>
                    </div>
                    <!-- Review Card 3 -->
                    <div
                        class="review-card relative bg-white p-6 rounded-lg shadow-xl transition-transform duration-500 hover:rounded-none hover:scale-110 border border-gray-100">
                        <!-- <div
                            class="absolute -top-0 -left-5 bg-gradient-to-r from-purple-500 to-purple-600 text-white w-14 h-14 rounded-full flex items-center justify-center shadow-lg">
                            <Icon name="lucide:user" class="!size-6" width="28" height="28" />
                        </div> -->
                        <div class="mx-8 mb-4 border-b border-gray-100 pb-3">
                            <h3 class="text-xl font-bold text-gray-800">Olivia Williams</h3>
                            <div class="flex items-center justify-between">
                                <p class="text-gray-500 text-sm">Guest</p>

                            </div>
                        </div>
                        <div class="relative">
                            <Icon name="lucide:quote" width="24" height="24"
                                class="text-gray-200 absolute -top-2 -left-1" />
                            <p class="text-gray-700 mb-3 pt-3 italic text-sm md:text-base pl-6">Very nice condo! Special
                                places arranged for the transfer
                                from the airport and everything went very smoothly. The condo was large and beautiful,
                                and
                                the third floor allowed for a lovely view...</p>
                            <Icon name="lucide:format-quote-close" width="24" height="24"
                                class="text-gray-200 absolute bottom-0 right-0" />
                        </div>
                        <div class="mt-4 pt-3 border-t border-gray-100 flex justify-end">
                            <div class="flex text-yellow-400">
                                <Icon v-for="i in 5" :key="i" name="lucide:star" width="16" height="16" class="ml-1" />
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Navigation arrows -->
                <!-- <button @click="goToPrev"
                    class="absolute left-2 top-1/2 -translate-y-1/2  p-3 rounded-full shadow-xl bg-white hover:bg-gray-50 hover:scale-110 transition-all duration-300 z-20 focus:outline-none focus:ring-2 focus:ring-blue-300 hidden md:flex items-center justify-center">
                    <Icon name="lucide:chevron-left" width="24" height="24" class="textColor !size-6" />
                </button>
                <button @click="goToNext"
                    class="absolute right-2 top-1/2 -translate-y-1/2  p-3 rounded-full bg-white shadow-xl hover:bg-gray-50 hover:scale-110 transition-all duration-300 z-20 focus:outline-none focus:ring-2 focus:ring-blue-300 hidden md:flex items-center justify-center">
                    <Icon name="lucide:chevron-right" width="24" height="24" class="textColor !size-6" />
                </button> -->

                <!-- Navigation dots (mobile friendly) -->
                <div class="absolute bottom-16 left-0 right-0 flex justify-center space-x-2">
                    <button v-for="(_, index) in 4" :key="index" @click="goToSlide(index)"
                        class="w-3 h-3 rounded-full transition-colors duration-200 focus:outline-none"
                        :class="currentIndex === index ? 'bg-[#4a8a9e]' : 'bg-gray-300'"></button>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">


const sliderRef = ref<HTMLElement | null>(null)
const currentIndex = ref(0)
const autoSlideInterval = ref<number | null>(null)

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
    if (index >= 0 && index <= 3) { // Updated to 4 cards
        currentIndex.value = index
        updateSlider()
        resetAutoSlide() // Reset the timer when manually changing slides
    }
}

// Start automatic slideshow
function startAutoSlide() {
    autoSlideInterval.value = window.setInterval(() => {
        const cards = sliderRef.value?.querySelectorAll('.review-card') || []
        if (currentIndex.value < cards.length - 1) {
            currentIndex.value++
        } else {
            currentIndex.value = 0 // Loop back to the first slide
        }
        updateSlider()
    }, 2000) // Change slide every 5 seconds
}

// Reset the automatic slideshow timer
function resetAutoSlide() {
    if (autoSlideInterval.value !== null) {
        clearInterval(autoSlideInterval.value)
        startAutoSlide()
    }
}

// function goToNext() {
//     if (!sliderRef.value) return

//     const cards = sliderRef.value.querySelectorAll('.review-card')
//     if (currentIndex.value < cards.length - 1) {
//         currentIndex.value++
//     } else {
//         currentIndex.value = 0 // Loop to the beginning
//     }
//     updateSlider()
//     resetAutoSlide()
// }

// function goToPrev() {
//     if (currentIndex.value > 0) {
//         currentIndex.value--
//     } else {
//         const cards = sliderRef.value?.querySelectorAll('.review-card') || []
//         currentIndex.value = cards.length - 1 // Loop to the end
//     }
//     updateSlider()
//     resetAutoSlide()
// }

onMounted(() => {
    // Make sure references are properly set after component is mounted
    updateSlider()
    // Start automatic slideshow
    startAutoSlide()
})

onBeforeUnmount(() => {
    // Clean up interval when component is unmounted
    if (autoSlideInterval.value !== null) {
        clearInterval(autoSlideInterval.value)
    }
})
</script>

<style scoped>
.review-card {
    scroll-snap-align: start;
    flex: 0 0 85%;
    transition: all 0.4s ease;
    transform-origin: center;
    backface-visibility: hidden;
}

@media (min-width: 768px) {
    .review-card {
        flex: 0 0 40%;
        max-width: 480px;
    }
}

.review-card:hover {
    box-shadow: 0 20px 25px -5px rgb(0 0 0 / 10%), 0 10px 10px -5px rgb(0 0 0 / 4%);
}

.review-slider {
    -ms-overflow-style: none;
    /* Hide scrollbar for IE and Edge */
    scrollbar-width: none;
    /* Hide scrollbar for Firefox */
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