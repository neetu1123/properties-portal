<template>
    <!-- <HomeBanner /> -->
    <div class="relative h-[45rem] overflow-hidden">
        <div class="flex h-full slide" style="width: 500%;">
            <!-- Slide 1 -->
            <div class="w-1/5 h-full bg-cover bg-center relative"
                style="background-image: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('/categories/golfcourse-scaled.jpg');">
                <div class="absolute inset-0 flex items-center justify-center text-center text-white px-4">
                    <div>
                        <h1 class="text-4xl md:text-6xl font-bold mb-4">Categories</h1>
                        <p class="text-lg md:text-xl mb-8 max-w-3xl">Your Ultimate Inlet Beach Escape — Thoughtfully
                            Curated for
                            Relaxation, Comfort, and Unforgettable Moments by the Sea</p>

                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="bg-gray-50 min-h-screen">
        <!-- List Page -->
        <div id="listPage" class="container mx-auto px-4 py-8">
            <!-- <h1 class="text-3xl font-bold text-gray-800 mb-8 text-center">Recreation Activities</h1> -->

            <!-- Activity Cards using v-for -->
            <div v-for="(category, index) in categoriesDetails" :key="category.id"
                class="overflow-hidden mb-8 lg:flex lg:items-center"
                :class="{ 'lg:flex-row-reverse': index % 2 !== 0 }">
                <div class="lg:w-1/2 rounded-2xl">
                    <img :src="category.image" :alt="category.title" class="rounded-2xl shadow-lg">
                </div>
                <div class="p-6 lg:w-1/2" :class="index % 2 === 0 ? 'lg:pl-8' : 'lg:pr-8'">
                    <h2 class="text-2xl font-bold text-gray-800 mb-4 flex items-center">
                        {{ category.title.toUpperCase() }}
                    </h2>
                    <p class="text-gray-600 mb-6 leading-relaxed">
                        {{ category.description }}
                    </p>
                    <button @click="navigateTo(`/categories/${category}`)"
                        class="bg-[#1B7895] hover:bg-[#5790a1] text-white px-6 py-3 rounded-full transition duration-300 flex items-center">
                        <Icon name="mdi:information" class="mr-2" />
                        Learn More
                    </button>
                </div>
            </div>
        </div>


    </div>
</template>

<script setup lang="ts">
const categoriesDetails = [
    {
        id: 'golf',
        title: 'Golf',
        description: 'Canyons Golf is an 18 hole, par 70 course with over 550 feet of elevation change. Conveniently located close to Sundial Lodge properties. Other nearby courses include Park City Golf Course, Mountain Dell, Wasatch Mountain and Soldier Hollow.',
        image: '/categories/golf-image.jpg',
        detailImage: 'detail-bg-1'
    },
    {
        id: 'hiking',
        title: 'Hiking',
        description: 'Blood Lake is an out and back in Park City\'s Bonanza Flats Conservation Area. Other popular hikes include Brighton Lakes Loop, Crystal and Watson Lakes, Albion Basin and many more.',
        image: '/categories/albionbasin-img.jpg',
        detailImage: 'detail-bg-2'
    },
    {
        id: 'lake',
        title: 'Lake',
        description: 'The Gauge Coffeehouse is a casual place to catch up with friends and offer drinks, homemade bagels and muffins. This is also the Chattooga Whitewater Shop where you\'ll find river gear, clothing and information about shuttle service to and from the river. Humble Pie Pizza is next door to The Gauge. It\'s a great place to unwind after a day exploring the area.',
        image: '/categories/alpine-img.jpg'
    },
    {
        id: 'boating',
        title: 'Boating',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/ballooning-img.jpg'
    },
    {
        id: 'aqua-park',
        title: 'Aqua Park',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/boatrental-img.jpg'
    },
    {
        id: 'tubing',
        title: 'River Tubing',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/discgolf-img.jpg'
    },
    {
        id: 'biking',
        title: 'Mountain Biking',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/fly-fishing-img.jpg'
    },
    {
        id: 'horseback',
        title: 'Horseback Riding',
        image: '/categories/aerial-img.jpg',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
    },
    {
        id: 'scenic',
        title: 'Scenic Drives',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/hebervalley-img.jpg'
    },
    {
        id: 'biking',
        title: 'Mountain Biking',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/horseback-img.jpg'
    },
    {
        id: 'fishing',
        title: 'Fly Fishing',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/kitesurf-img.jpg'
    },
    {
        id: 'rafting',
        title: 'Rafting',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/lake-activities-img.jpg'
    },
    {
        id: 'ziplines',
        title: 'Ziplines',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/mountain-biking-img.jpg'
    },
    {
        id: 'slide',
        title: 'Alpine Slide',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/provo-river-tubing-img.jpg'
    },
    {
        id: 'ebikes',
        title: 'Electric Bikes',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/rafting-img.jpg'
    },
    {
        id: 'railroad',
        title: 'Scenic Railroad',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/scenic-drives-img.jpg'
    },
    {
        id: 'kiteboarding',
        title: 'Kiteboarding',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/trail-rides.jpg'
    },
    {
        id: 'ballooning',
        title: 'Ballooning',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/wibit-img.jpg'
    },
    {
        id: 'freestyle',
        title: 'Freestyle Aerials',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/zipline-img.jpg'
    },
    {
        id: 'disc-golf',
        title: 'Disc Golf',
        description: 'This is a wonderful place to walk around, eat lunch, pick fruit from the orchard, shop for souvenirs, sample distilled spirits, play ultimate frisbee. You can actually walk to Chattooga Belle Farm from Moretown Bunkhouse. Go down to the end of Kenneth Road (away from Hwy 76), cross over a dam (there are no trespassing signs, but this is actually a public dam) and walk up to Chattooga Belle Farm and the Distillery. Takes maybe 30 minutes to walk there.',
        image: '/categories/zipline-img.jpg'
    },
]
</script>
