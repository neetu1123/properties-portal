<template>
    <div class="bg-gray-50 py-16">
        <!-- Font Awesome -->
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />

        <!-- Why Stay With Savvy Section -->
        <div class="container mx-auto px-4">
            <div class="grid lg:grid-cols-2 gap-12 items-center">
                <!-- Left Content -->
                <div>
                    <h2 class="text-4xl font-bold text-gray-900 mb-6">
                        Why Stay With A Curated Vacation?
                    </h2>
                    <p class="text-gray-600 mb-8 leading-relaxed">
                        Lorem ipsum, dolor sit am quae earum reiciendis possimus maxime consequatur porro placeat,
                        suscipit tus minima quia quis exercitationem ea architecto ullam nulla veniam
                        dolorum autem ipsam vero, tempora odio. Nihil architecto voluptas molestiae ratione neque fuga
                        ipsa.
                    </p>

                    <!-- Features Grid -->
                    <div class="grid grid-cols-2 gap-6 mb-8 ml-2">
                        <div v-for="(feature, index) in features" :key="index" class="flex items-center space-x-3">
                            <div :class="`${feature.color} bg-[#91d2e6] p-2 rounded-lg`">
                                <Icon :name="feature.iconClass" class="textColor !size-5" />
                            </div>
                            <span class="text-gray-700 font-medium">{{ feature.title }}</span>
                        </div>
                    </div>

                    <!-- Book Now Button -->
                    <button
                        class="bgGradient hover:bg-[#5790a1] hover:scale-110 transition-all duration-300 text-white px-8 ml-2 py-4 justify-center rounded-lg font-semibold transition-colors duration-200 flex items-center space-x-2">
                        <span>Book Now </span>
                        <Icon name="lucide:arrow-right" class="!size-4" />
                    </button>
                </div>

                <!-- Right Image -->
                <div class="relative">
                    <div class="rounded-3xl overflow-hidden shadow-2xl">
                        <img src="/ABout Us_11zon.jpg"
                            alt="Luxury vacation rental with pool" class="w-full h-full object-cover" />
                        <!-- Partner Badges -->
                        <div class="absolute -bottom-10 right-52 flex space-x-6">
                            <div class="bg-white rounded-lg p-3 px-8  shadow-lg flex">

                                <div class="px-2">
                                    <img src="/AirBnB.jpg" alt="">
                                </div>
                                <div class=" px-4">
                                    <img src="/Vrbo.jpg" alt="">
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">

const features = [
    {
        iconClass: 'lucide:hotel',
        title: "24/7 Guest Concierge",
        color: "text-orange-500"
    },
    {
        iconClass: 'lucide:shield-user',
        title: "Hotel Amenities",
        color: "text-orange-500"
    },
    {
        iconClass: 'lucide:user-check',
        title: "Seamless Check-in",
        color: "text-orange-500"
    },
    {
        iconClass: 'lucide:user',
        title: "Family Friendly",
        color: "text-orange-500"
    },
    {
        iconClass: 'lucide:wifi',
        title: "Blazing Fast WiFi",
        color: "text-orange-500"
    },
    {
        iconClass: 'lucide:sparkles',
        title: "Professionally Cleaned",
        color: "text-orange-500"
    }
]

</script>

<style scoped>
/* Create simple icon components to replace the Lucide React icons */
.hotel-icon,
.shield-icon,
.user-check-icon,
.users-icon,
.wifi-icon,
.sparkles-icon {
    width: 24px;
    height: 24px;
    display: inline-block;
}
</style>
