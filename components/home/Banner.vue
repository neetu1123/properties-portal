<template>
    <!-- Banner Slider -->
    <div class="relative h-screen overflow-hidden">
        <div class="flex h-full slide" style="width: 500%;">
            <!-- Slide 1 -->
            <div class="w-1/5 h-full bg-cover bg-center relative"
                style="background-image: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('/Beach Image.jpg');">
                <div class="absolute inset-0 flex items-center justify-center text-center text-white px-4">
                    <div>
                        <h1 class="text-4xl md:text-6xl font-bold mb-4">A Curated Vacation</h1>
                        <p class="text-lg md:text-xl mb-8 max-w-3xl">Your Ultimate Inlet Beach Escape — Thoughtfully Curated for Relaxation, Comfort, and Unforgettable Moments by the Sea</p>
                        <button
                            class="bgGradient hover:bg-[#5790a1] hover:scale-110 duration-300 text-white px-8 py-3 rounded-full font-medium text-lg transition-colors">
                            Book Now
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
.slide {
    transition: transform 0.5s ease-in-out;
}

.dot {
    transition: all 0.3s ease;
}

.dot.active {
    background-color: #fff;
    transform: scale(1.2);
}
</style>