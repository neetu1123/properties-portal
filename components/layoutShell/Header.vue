<template>
    <!-- Navigation Bar -->
    <nav class="bg-[#004369] opacity-70 shadow-md fixed w-full top-0 z-50">
        <div class="container mx-auto">
            <div class="flex  items-center h-20">
                <!-- Logo -->
                <div class="flex items-center">
                    <h1 class="">
                        <img src="/A_Curated_Vacation_logo_page-0001__1_-removebg-preview.png" class="h-12" alt="">
                    </h1>
                </div>
                <div class="flex-1 flex justify-end items-center">

                    <!-- Desktop Navigation -->
                    <div class="hidden md:flex items-center space-x-8">
                        <button class="bg-[#1B7895] hover:bg-[#5790a1] hover:scale-110 duration-300 text-white px-6 py-2 rounded-full font-medium transition-colors">
                            Book
                        </button>
                        <a href="#" class="text-white hover:text-lightText font-medium transition-colors">Location</a>
                        <a href="#" class="text-white hover:text-lightText font-medium transition-colors">Photos</a>
                        <a href="#" class="text-white hover:text-lightText font-medium transition-colors">Rates</a>
                        <a href="#"
                            class="text-white hover:text-lightText font-medium transition-colors">Availability</a>
                        <a href="#" class="text-white hover:text-lightText font-medium transition-colors">Reviews</a>
                    </div>

                    <!-- Social Icons -->
                    <div class="hidden md:flex items-center space-x-4 ml-12">
                        <a href="#" class="text-white hover:text-lightText transition-colors">
                            <Icon name="lucide:facebook" width="20" class="!size-5" height="20" />
                        </a>
                        <a href="#" class="text-white hover:text-lightText transition-colors">
                            <Icon name="lucide:instagram" width="20" class="!size-5" height="20" />
                        </a>
                        <a href="#" class="text-white hover:text-lightText transition-colors">
                            <img src="/video.png" alt="" class="w-7 h-7">
                        </a>

                    </div>
                </div>

                <!-- Mobile Menu Button -->
                <div class="md:hidden">
                    <button @click="toggleMobileMenu" class="text-white hover:text-lightText transition-colors">
                        <Icon name="lucide:menu" width="24" height="24" />
                    </button>
                </div>
            </div>

            <!-- Mobile Menu -->
            <div v-show="mobileMenuOpen" class="md:hidden pb-4">
                <div class="flex flex-col space-y-2">
                    <button
                        class="bg-gradient-to to-lightText from-textColor hover:bg-[#1B7895] text-white px-4 py-2 rounded-full font-medium transition-colors text-center">
                        Book
                    </button>
                    <a href="#"
                        class="text-gray-700 hover:text-orange-500 font-medium py-2 transition-colors">Location</a>
                    <a href="#"
                        class="text-gray-700 hover:text-orange-500 font-medium py-2 transition-colors">Photos</a>
                    <a href="#" class="text-gray-700 hover:text-orange-500 font-medium py-2 transition-colors">Rates</a>
                    <a href="#"
                        class="text-gray-700 hover:text-orange-500 font-medium py-2 transition-colors">Availability</a>
                    <a href="#"
                        class="text-gray-700 hover:text-orange-500 font-medium py-2 transition-colors">Reviews</a>
                </div>
            </div>
        </div>
    </nav>
</template>

<script setup lang="ts">
const mobileMenuOpen = ref(false)

function toggleMobileMenu() {
    mobileMenuOpen.value = !mobileMenuOpen.value;
}

</script>
