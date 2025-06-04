<template>
    <!-- Testimonials Section -->
    <div class="bg-gray-50 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mb-20">
            <div class="text-center mb-12">
                <p class="lightText text-sm font-medium mb-2">testimonials</p>
                <h2 class="text-4xl font-bold text-gray-900 mb-4">
                    Guest <span class="lightText">Reviews</span>
                </h2>
                <p class="text-gray-600 max-w-2xl mx-auto">
                    Get inspired by glowing guest reviews that showcase the exceptional experiences and
                    unforgettable memories created by the staff at Special Places of Costa Rica.
                </p>
            </div>

            <div class="relative">
                <div class="bg-[#4a8a9e] transform rounded-3xl p-20 relative overflow-hidden">
                    <div class="flex justify-center items-center space-x-8">
                        <!-- Previous testimonial (partially visible) -->
                        <div class="hidden lg:block w-80 opacity-50 transform scale-95">
                            <div class="bg-white rounded-2xl p-6 shadow-lg">
                                <div class="flex items-center mb-4">
                                    <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center">
                                        <div class="w-8 h-8 bg-blue-500 rounded-lg flex items-center justify-center">
                                            <div class="w-4 h-4 bg-yellow-400 rounded"></div>
                                        </div>
                                    </div>
                                    <div class="ml-4">
                                        <h4 class="font-semibold text-gray-900">{{ testimonials[(currentSlide - 1 + 3) %
                                            3].name }}</h4>
                                        <p class="text-gray-500 text-sm">{{ testimonials[(currentSlide - 1 + 3) %
                                            3].role }}</p>
                                    </div>
                                </div>
                                <p class="text-gray-600 text-sm mb-4 line-clamp-4">
                                    {{ testimonials[(currentSlide - 1 + 3) % 3].text }}
                                </p>
                                <div class="flex space-x-1">
                                    <span v-for="star in 5" :key="star" class="text-yellow-400">★</span>
                                </div>
                            </div>
                        </div>

                        <!-- Current testimonial (center) -->
                        <div class="w-80 transform scale-100">
                            <div class="bg-white rounded-2xl p-6 shadow-lg">
                                <div class="flex items-center mb-4">
                                    <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center">
                                        <div class="w-8 h-8 bg-blue-500 rounded-lg flex items-center justify-center">
                                            <div class="w-4 h-4 bg-yellow-400 rounded"></div>
                                        </div>
                                    </div>
                                    <div class="ml-4">
                                        <h4 class="font-semibold text-gray-900">{{ testimonials[currentSlide].name }}
                                        </h4>
                                        <p class="text-gray-500 text-sm">{{ testimonials[currentSlide].role }}</p>
                                    </div>
                                </div>
                                <p class="text-gray-600 text-sm mb-4">
                                    {{ testimonials[currentSlide].text }}
                                </p>
                                <div class="flex space-x-1">
                                    <span v-for="star in 5" :key="star" class="text-yellow-400">★</span>
                                </div>
                            </div>
                        </div>

                        <!-- Next testimonial (partially visible) -->
                        <div class="hidden lg:block w-80 opacity-50 transform scale-95">
                            <div class="bg-white rounded-2xl p-6 shadow-lg">
                                <div class="flex items-center mb-4">
                                    <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center">
                                        <div class="w-8 h-8 bg-blue-500 rounded-lg flex items-center justify-center">
                                            <div class="w-4 h-4 bg-yellow-400 rounded"></div>
                                        </div>
                                    </div>
                                    <div class="ml-4">
                                        <h4 class="font-semibold text-gray-900">{{ testimonials[(currentSlide + 1) %
                                            3].name }}</h4>
                                        <p class="text-gray-500 text-sm">{{ testimonials[(currentSlide + 1) % 3].role }}
                                        </p>
                                    </div>
                                </div>
                                <p class="text-gray-600 text-sm mb-4 line-clamp-4">
                                    {{ testimonials[(currentSlide + 1) % 3].text }}
                                </p>
                                <div class="flex space-x-1">
                                    <span v-for="star in 5" :key="star" class="text-yellow-400">★</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Navigation dots -->
                    <div class="flex justify-center mt-8 space-x-2">
                        <button v-for="index in 3" :key="index - 1" @click="goToSlide(index - 1)"
                            class="w-3 h-3 rounded-full transition-colors duration-200"
                            :class="currentSlide === index - 1 ? 'bg-[#1B7895]' : 'bg-gray-300'"></button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">

const currentSlide = ref(1)
const testimonials = [
    {
        id: 1,
        name: "Ethan Parker",
        role: "Guest",
        text: "La Casa Roja è molto bella e comoda. Noi eravamo in 6 con un cagnolino e siamo stati benissimo. Molto pulita e spaziosa. Tutti gli ambienti sono comodi e piacevoli. La piscina è molto comoda per rinfrescarsi al rientro dal mare. Ogni giorno ci facevano visita ...",
        rating: 5
    },
    {
        id: 2,
        name: "Ava Thompson",
        role: "Guest",
        text: "ncreible lugar ! Una vista espectacular definitivamente en el paraiso , muy confortable y muy amables y seguro y mucha privacidad super recomendado perfecta ubicacion cerca de muchas playas de guanacaste",
        rating: 5
    },
    {
        id: 3,
        name: "Olivia Williams",
        role: "Guest",
        text: "Very nice condo! Special places arranged for the transfer from the airport and everything went very smoothly. The condo was large and beautiful, and the third floor allowed for a lovely view right at the level of the tree canopy. The pools and ...",
        rating: 5
    }
]

function nextSlide() {
    currentSlide.value = (currentSlide.value + 1) % 3;
}
function prevSlide() {
    currentSlide.value = (currentSlide.value - 1 + 3) % 3;
}
function goToSlide(index: number) {
    currentSlide.value = index;
}

</script>

<style scoped>
.line-clamp-4 {
    display: -webkit-box;
    -webkit-line-clamp: 4;
    -webkit-box-orient: vertical;
    overflow: hidden;
}
</style>