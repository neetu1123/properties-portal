<template>
    <div class="bg-gray-50 py-20 px-4 sm:px-6 lg:px-8">
        <div class="container mx-auto">
            <!-- Header -->
            <div class="text-center mb-12">
                <h2 class="text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
                    Attractions
                </h2>
                <p class="text-lg text-gray-600 max-w-3xl mx-auto">
                    Fun for All Ages — From Sandy Shores to Local Adventures
                </p>
            </div>

            <!-- Destinations Slider -->
            <div class="relative">
                <!-- Navigation Buttons -->
                 <button @click="prevSlide"
                    class="absolute left-2 top-1/2 -translate-y-1/2  p-3 rounded-full bg-white shadow-xl hover:bg-gray-50 hover:scale-110 transition-all duration-300 z-20 focus:outline-none focus:ring-2 focus:ring-blue-300 hidden md:flex items-center justify-center">
                    <Icon name="lucide:chevron-left" width="24" height="24" class="textColor !size-6" />
                </button>

                 <button @click="nextSlide"
                    class="absolute right-2 top-1/2 -translate-y-1/2  p-3 rounded-full bg-white shadow-xl hover:bg-gray-50 hover:scale-110 transition-all duration-300 z-20 focus:outline-none focus:ring-2 focus:ring-blue-300 hidden md:flex items-center justify-center">
                    <Icon name="lucide:chevron-right" width="24" height="24" class="textColor !size-6" />
                </button>

                <!-- Destinations Grid -->
                <div class="overflow-hidden mx-12">
                    <div class="flex transition-transform duration-300 ease-in-out"
                        :style="{ transform: `translateX(-${currentIndex * 20}%)` }">
                        <div v-for="(destination, index) in destinations" :key="index" class="w-1/5 flex-shrink-0 px-2">
                            <div
                                class="rounded-xl overflow-hidden">
                                 <div class="p-4 text-center">
                                    <h3 class="text-xl font-bold text-gray-900 mb-2">{{ destination.name }}</h3>
                                    <div class="w-8 h-1 bg-[#1B7895] mx-auto"></div>
                                </div>
                                <div class="relative h-64 ">
                                    <img :src="destination.image" :alt="destination.name"
                                        class="w-full h-full object-cover rounded-xl" />
                                    <div class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent"></div>
                                </div>
                               
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- View All Button -->
            <div class="text-center mt-12">
                <button
                    class="bgGradient text-white px-8 py-3 rounded-lg font-semibold transition-colors inline-flex items-center">
                    View All 
                    <Icon name="lucide:arrow-right" class="!size-5 ml-2" /> 
                </button>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">

const currentIndex = ref(0)
const destinations = [
    {
        name: " Rosemary Beach",
        image: "/Rosemary Beach.jpg"
    },
    {
        name: "Timpoochee Trail",
        image: "/Timpoochee Trail_11zon.jpg"
    },
    {
        name: "Camp Helen State Park",
        image: "/Camp Helen State Park_11zon.webp"
    },
    {
        name: "30Avenue",
        image: "/30Avenue.jpg"
    },
    {
        name: "Alys Beach",
        image: "/Alys Beach_11zon.jpg"
    },
    {
        name: " Rosemary Beach",
        image: "/Rosemary Beach.jpg"
    },
]

function nextSlide() {
    currentIndex.value = (currentIndex.value + 1) % Math.max(1, destinations.length - 4);
}
function prevSlide() {
    currentIndex.value = (currentIndex.value - 1 + Math.max(1, destinations.length - 4)) % Math.max(1, destinations.length - 4);
}

</script>

<style scoped>
/* Add component-specific styles here */
</style>