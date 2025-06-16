<template>
    <div class="container mx-auto mt-24 px-4 py-6 bg-gray-50">
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            <!-- Main Content -->
            <div class="col-span-2">
                <!-- Hero Image -->
                <div class="mb-6 ">
                    <img src="https://images.unsplash.com/photo-1544551763-46a013bb70d5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80"
                        alt="Aerial view of St. Augustine, Florida at sunset"
                        class="w-full h-96 rounded-lg shadow-lg">
                </div>

                <!-- Article Header -->
                <div class="mb-6">
                    <h1 class="text-2xl md:text-3xl lg:text-4xl font-bold text-blue-gray mb-4">
                        Top 10 Things To Do In St. Augustine, Florida
                    </h1>

                    <div class="flex flex-wrap items-center gap-4 text-sm text-gray-500 mb-6">
                        <div class="flex items-center gap-2">
                            <Icon name="mdi:calendar" class="text-coral" />
                            <span>24 Jul 2023</span>
                        </div>
                        <div class="flex items-center gap-2">
                            <Icon name="mdi:tag" class="text-coral" />
                            <span>Things to Do</span>
                        </div>
                    </div>

                    <h2 class="text-lg font-semibold text-gray-800 mb-4">
                        Top 10 Things to Do in St. Augustine, Florida
                    </h2>

                    <p class="text-gray-600 leading-relaxed mb-8">
                        St. Augustine, Florida, is a charming, historic city that offers a perfect blend of culture,
                        history, and natural beauty. As the oldest city in the United States, it's rich in stories,
                        stunning architecture, and unique attractions. Whether you're a history buff, an art lover, or
                        someone who enjoys coastal beauty, St. Augustine has something for everyone. Here are the top 10
                        things to do in this captivating destination:
                    </p>
                </div>

                <!-- Article Content -->
                <div class="space-y-8">
                    <!-- Item 1 -->
                    <div>
                        <h3 class="text-xl font-semibold text-blue-gray mb-4">
                            1. Explore Castillo de San Marcos
                        </h3>
                        <p class="text-gray-600 leading-relaxed">
                            No visit to St. Augustine is complete without a trip to Castillo de San Marcos, the oldest
                            masonry fort in the continental United States. This 17th-century fort offers an exciting
                            glimpse into the city's colonial past. Stroll through the well-preserved grounds, learn
                            about its history, and take in the beautiful views of the Matanzas Bay.
                        </p>
                    </div>

                    <!-- Item 2 -->
                    <div>
                        <h3 class="text-xl font-semibold text-blue-gray mb-4">
                            2. Walk Along St. George Street
                        </h3>
                        <p class="text-gray-600 leading-relaxed">
                            St. George Street is a pedestrian-only street lined with charming shops, cafes, and
                            historical landmarks. As you stroll down this cobblestone street, you'll find an array of
                            boutiques, art galleries, and cozy spots to stop for a bite to eat. It's the perfect place
                            to soak in the atmosphere of the city.
                        </p>
                    </div>

                    <!-- Item 3 -->
                    <div>
                        <h3 class="text-xl font-semibold text-blue-gray mb-4">
                            3. Visit the Lightner Museum
                        </h3>
                        <p class="text-gray-600 leading-relaxed">
                            Housed in the former Alcazar Hotel, the Lightner Museum is a treasure trove of fine and
                            decorative art from the 19th and early 20th centuries. This museum displays everything from
                            Tiffany glass to Victorian-era furniture, and the building itself is a stunning piece of
                            architecture.
                        </p>
                    </div>

                    <!-- Item 4 -->
                    <div>
                        <h3 class="text-xl font-semibold text-blue-gray mb-4">
                            4. Take a Ghost Tour
                        </h3>
                        <p class="text-gray-600 leading-relaxed">
                            St. Augustine is known for its haunted history. The city offers several ghost tours, where
                            you can explore the spookier side of this ancient town. From the Old Jail to the Ghosts and
                            Gravestones Tour, you'll hear eerie tales and visit some of the most haunted spots in the
                            city. Perfect for those who love a good thrill!
                        </p>
                    </div>

                    <!-- Item 5 -->
                    <div>
                        <h3 class="text-xl font-semibold text-blue-gray mb-4">
                            5. Relax at St. Augustine Beach
                        </h3>
                        <p class="text-gray-600 leading-relaxed">
                            St. Augustine Beach is a beautiful, relaxing spot to unwind. The wide, sandy beach is
                            perfect for sunbathing, beachcombing, or enjoying a picnic by the ocean. You can also rent
                            bikes or paddleboards to explore the coastline or simply enjoy the stunning views.
                        </p>
                    </div>
                </div>
            </div>

            <!-- Sidebar -->
            <div class="lg:col-span-1">
                <div class="space-y-8">
                    <!-- Categories -->
                    <div class="bg-white rounded-xl shadow-xl p-8 ">
                        <h3 class="text-lg font-semibold text-coral mb-8 underline ">
                            Categories
                        </h3>
                        <ul class="space-y-3">
                            <li>
                                <a href="#"
                                    class="flex items-center border-b border-gray-200 pb-2 justify-between text-gray-600 hover:text-coral transition-colors duration-200">
                                    <span>Things to Do</span>
                                    <span class="text-sm text-gray-400">(1)</span>
                                </a>
                            </li>
                        </ul>
                    </div>

                    <!-- Recent Posts -->
                    <div class="bg-white rounded-lg shadow-md p-6">
                        <h3 class="text-lg font-semibold text-coral mb-4 border-b border-gray-200 pb-2">
                            Recent Posts
                        </h3>
                        <div class="text-sm text-gray-500">
                            No recent posts to display
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
// Define page title and meta
useHead({
    title: 'Top 10 Things To Do In St. Augustine, Florida',
})

// You can add Nuxt specific functionality here
// For example, fetch blog data based on the [blogId] route parameter:
// const route = useRoute();
// const { data: blogPost } = await useFetch(`/api/blogs/${route.params.blogId}`);
</script>

<style scoped>
/* Add any component-specific styles here */
</style>