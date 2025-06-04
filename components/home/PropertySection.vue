<template>
    <div class="bg-gray-50 py-16 px-4 sm:px-6 lg:px-8">
        <div class="container mx-auto">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <!-- Image Section -->
                <div class="relative">
                    <img src="https://images.unsplash.com/photo-1566073771259-6a8506099945?w=600&h=400&fit=crop&crop=center"
                        alt="Ocean View Terrace" class="w-full h-full object-cover rounded-lg shadow-2xl" />
                   
                </div>

                <!-- Content Section -->
                <div>
                    <div class="mb-6">
                        <h3 class="lightText font-semibold text-lg mb-2">Property Details</h3>
                        <h2 class="text-4xl font-bold text-gray-900 mb-4">Ocean View Bliss</h2>
                        <div class="flex items-center text-gray-600 mb-6">
                            <Icon name="lucide:map-marker" width="20" height="20" class="mr-2" />
                            <span>53 Sheridan Ave, Seaside Heights, NJ 08751, USA</span>
                        </div>
                    </div>

                    <p class="text-gray-700 leading-relaxed mb-8">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla, reiciendis repellendus! Unde ab sed minima vero asperiores neque explicabo exercitationem quam, ipsum aperiam ex id at, obcaecati quas sapiente rem iure suscipit voluptatibus atque nisi harum alias? Obcaecati voluptas consequatur labore. Dolore odit numquam soluta quaerat vel illum ratione, itaque officiis animi distinctio error dolores, voluptas rem sint culpa delectus harum, deserunt natus asperiores sed! Fuga vero eos ad voluptates blanditiis, neque fugiat reprehenderit perspiciatis recusandae distinctio alias aliquam cumque?
                    </p>

                    <div class="mb-8">
                        <p class="text-2xl font-bold text-gray-900">Starting from $450 / Night</p>
                    </div>

                    <!-- Property Features -->
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-6 border-t border-b border-gray-200 py-6">
                        <div class="text-center">
                            <Icon name="lucide:bed" width="32" height="32" class="mx-auto !size-6 mb-2 textColor" />
                            <p class="font-semibold text-gray-900">5 Bedrooms</p>
                        </div>
                        <div class="text-center">
                            <Icon name="lucide:shower-head" width="32" height="32" class="mx-auto !size-6 mb-2 textColor" />
                            <p class="font-semibold text-gray-900">3.5 Baths</p>
                        </div>
                        <div class="text-center">
                            <Icon name="lucide:shower-head" width="32" height="32" class="mx-auto !size-6 mb-2 textColor" />
                            <p class="font-semibold text-gray-900">1 Outside Shower</p>
                        </div>
                        <div class="text-center">
                            <Icon name="lucide:contact-round" width="32" height="32" class="mx-auto !size-6 mb-2 textColor" />
                            <p class="font-semibold text-gray-900">12 Guests</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>