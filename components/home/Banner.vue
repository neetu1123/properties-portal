<template>
    <!-- Banner Slider -->
    <div class="relative h-screen overflow-hidden">
        <div ref="slider" class="flex h-full slide" style="width: 500%;">
            <!-- Slide 1 -->
            <div class="w-1/5 h-full bg-cover bg-center relative"
                style="background-image: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('/photo-1518684079-3c830dcef090.jpeg');">
                <div class="absolute inset-0 flex items-center justify-center text-center text-white px-4">
                    <div>
                        <h1 class="text-4xl md:text-6xl font-bold mb-4">Absolute Bearadise</h1>
                        <p class="text-lg md:text-xl mb-8 max-w-2xl">Your perfect Smoky Mountain getaway with hot tub,
                            arcade games, and breathtaking views</p>
                        <button
                            class="bgGradient text-white px-8 py-3 rounded-full font-medium text-lg transition-colors">
                            Book Now
                        </button>
                    </div>
                </div>
            </div>

            <!-- Slide 2 -->
            <div class="w-1/5 h-full bg-cover bg-center relative"
                style="background-image: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('/photo-1506905925346-21bda4d32df4.avif');">
                <div class="absolute inset-0 flex items-center justify-center text-center text-white px-4">
                    <div>
                        <h1 class="text-4xl md:text-6xl font-bold mb-4">Luxury Hot Tub</h1>
                        <p class="text-lg md:text-xl mb-8 max-w-2xl">Relax under the stars in our premium hot tub with
                            mountain views</p>
                        <button
                            class="bgGradient text-white px-8 py-3 rounded-full font-medium text-lg transition-colors">
                            Book Now
                        </button>
                    </div>
                </div>
            </div>

            <!-- Slide 3 -->
            <div class="w-1/5 h-full bg-cover bg-center relative"
                style="background-image: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('/photo-1518684079-3c830dcef090.jpeg');">
                <div class="absolute inset-0 flex items-center justify-center text-center text-white px-4">
                    <div>
                        <h1 class="text-4xl md:text-6xl font-bold mb-4">Game Room</h1>
                        <p class="text-lg md:text-xl mb-8 max-w-2xl">Enjoy hours of fun with arcade games and
                            entertainment for all ages</p>
                        <button
                            class="bgGradient text-white px-8 py-3 rounded-full font-medium text-lg transition-colors">
                            Book Now
                        </button>
                    </div>
                </div>
            </div>

            <!-- Slide 4 -->
            <div class="w-1/5 h-full bg-cover bg-center relative"
                style="background-image: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('/photo-1571896349842-33c89424de2d.avif');">
                <div class="absolute inset-0 flex items-center justify-center text-center text-white px-4">
                    <div>
                        <h1 class="text-4xl md:text-6xl font-bold mb-4">Mountain Views</h1>
                        <p class="text-lg md:text-xl mb-8 max-w-2xl">Wake up to stunning Smoky Mountain vistas every
                            morning</p>
                        <button
                            class="bgGradient text-white px-8 py-3 rounded-full font-medium text-lg transition-colors">
                            Book Now
                        </button>
                    </div>
                </div>
            </div>

            <!-- Slide 5 -->
            <div class="w-1/5 h-full bg-cover bg-center relative"
                style="background-image: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('/photo-1587825140708-dfaf72ae4b04.avif');">
                <div class="absolute inset-0 flex items-center justify-center text-center text-white px-4">
                    <div>
                        <h1 class="text-4xl md:text-6xl font-bold mb-4">Cozy Interior</h1>
                        <p class="text-lg md:text-xl mb-8 max-w-2xl">Experience comfort and luxury in our beautifully
                            appointed cabin</p>
                        <button
                            class="bgGradient text-white px-8 py-3 rounded-full font-medium text-lg transition-colors">
                            Book Now
                        </button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Navigation Arrows -->
        <button @click="prevSlide"
            class="absolute left-4 top-1/2 transform -translate-y-1/2">
            <Icon name="lucide:circle-chevron-left" class="!size-8 textColor" width="24" height="24" />
        </button>
        <button @click="nextSlide"
            class="absolute right-4 top-1/2 transform -translate-y-1/2">
            <Icon name="lucide:circle-chevron-right" class="!size-8 textColor" width="24" height="24" />
        </button>

        <!-- Dots Indicator -->
        <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 flex space-x-3">
            <button v-for="(_, index) in 5" :key="index" @click="goToSlide(index)"
                class="dot w-3 h-3 rounded-full bg-white bg-opacity-50 hover:bg-opacity-75 transition-all"
                :class="{ 'active': currentSlide === index }"></button>
        </div>
    </div>
</template>

<script setup lang="ts">

const currentSlide = ref(0)
const totalSlides = ref(5)
const autoSlideInterval = ref()
const slider = ref<HTMLElement | null>(null)

onMounted(() => {
    // Start auto-slide
    startAutoSlide();
    // Initialize slider
    updateSlider();
}),
    onBeforeUnmount(() => {
        // Clear interval when component is destroyed
        clearInterval(autoSlideInterval.value);
    })

function updateSlider() {
    if (slider.value) {
        const translateX = -currentSlide.value * 20; // Each slide is 20% (1/5) of total width
        slider.value.style.transform = `translateX(${translateX}%)`;
    }
    }

function nextSlide() {
    currentSlide.value = (currentSlide.value + 1) % totalSlides.value;
    updateSlider();
}
function prevSlide() {
    currentSlide.value = (currentSlide.value - 1 + totalSlides.value) % totalSlides.value;
    updateSlider();
}
function goToSlide(index: number) {
    currentSlide.value = index;
    updateSlider();
}
function startAutoSlide() {
    autoSlideInterval.value = setInterval(nextSlide, 5000); // Auto slide every 5 seconds
}

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