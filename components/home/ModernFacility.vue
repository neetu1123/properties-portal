<template>
    <div class="bg-white py-16 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
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

            <!-- Additional Features -->
            <div class="mt-16 bg-gray-50 rounded-2xl p-8 lg:p-12">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-center">
                    <div>
                        <h3 class="text-2xl lg:text-3xl font-bold text-gray-900 mb-6">
                            Premium Amenities for Your Comfort
                        </h3>
                        <div class="space-y-4">
                            <div class="flex items-center">
                                <Icon name="lucide:check-circle" width="20" height="20" class="text-green-500 mr-3" />
                                <span class="text-gray-700">High-speed WiFi throughout the property</span>
                            </div>
                            <div class="flex items-center">
                                <Icon name="lucide:check-circle" width="20" height="20" class="text-green-500 mr-3" />
                                <span class="text-gray-700">Smart TV with streaming services</span>
                            </div>
                            <div class="flex items-center">
                                <Icon name="lucide:check-circle" width="20" height="20" class="text-green-500 mr-3" />
                                <span class="text-gray-700">Fully equipped modern kitchen</span>
                            </div>
                            <div class="flex items-center">
                                <Icon name="lucide:check-circle" width="20" height="20" class="text-green-500 mr-3" />
                                <span class="text-gray-700">Washer and dryer included</span>
                            </div>
                        </div>
                    </div>
                    <div class="grid grid-cols-2 gap-4">
                        <div class="bg-white p-6 rounded-lg text-center">
                            <Icon name="lucide:wifi" width="32" height="32"
                                class="!size-8 lightText mx-auto mb-3" />
                            <p class="font-semibold text-gray-900">Free WiFi</p>
                        </div>
                        <div class="bg-white p-6 rounded-lg text-center">
                            <Icon name="lucide:car" width="32" height="32"
                                class="!size-8 lightText mx-auto mb-3" />
                            <p class="font-semibold text-gray-900">Free Parking</p>
                        </div>
                        <div class="bg-white p-6 rounded-lg text-center">
                            <Icon name="lucide:hotel" width="32" height="32"
                                class="!size-8 lightText mx-auto mb-3" />
                            <p class="font-semibold text-gray-900">Hot Tub</p>
                        </div>
                        <div class="bg-white p-6 rounded-lg text-center">
                            <Icon name="lucide:gamepad" width="32" height="32"
                                class="!size-8 lightText mx-auto mb-3" />
                            <p class="font-semibold text-gray-900">Game Room</p>
                        </div>
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
