<template>
    <div class="bg-white py-16 px-4 sm:px-6 lg:px-8">
        <div class="container mx-auto">
            <!-- Header -->
            <div class="text-center mb-16">
                <p class=" font-medium text-lg mb-4 textColor">Built for Comfort</p>
                <h2 class="text-4xl lg:text-5xl font-bold text-gray-900">
                    Modern Facilities
                </h2>
            </div>

            <!-- Facilities Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div v-for="(facility, index) in facilities" :key="index"
                    class="text-center group hover:transform hover:scale-105 transition-all duration-300">
                    <!-- Icon -->
                    <div class="mb-6">
                        <div
                            class="w-20 h-20 mx-auto bg-[#91d2e6] rounded-full flex items-center justify-center transition-colors">
                            <Icon :name="facility.icon" class="textColor !size-10" />
                        </div>
                    </div>

                    <!-- Content -->
                    <div>
                        <h3 class="text-xl font-bold text-gray-900 mb-4">{{ facility.title }}</h3>
                        <p class="text-gray-600 leading-relaxed">{{ facility.description }}</p>
                    </div>
                </div>
            </div>


        </div>
    </div>
</template>

<script setup lang="ts">

const facilities = [
    {
        icon: "lucide:monitor-pause",
        title: "Smart Home System",
        description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem nobis enim consequuntur aliquam ."
    },
    {
        icon: "lucide:badge-japanese-yen",
        title: "Solar Energy Panels",
        description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem nobis enim consequuntur aliquam ."
    },
    {
        icon: "lucide:snowflake",
        title: "Central Air Conditioning",
        description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem nobis enim consequuntur aliquam ."
    },
    {
        icon: "lucide:home",
        title: "Home Security System",
        description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem nobis enim consequuntur aliquam ."
    }
]
</script>
