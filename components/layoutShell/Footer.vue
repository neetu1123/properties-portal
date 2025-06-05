<template>
    <footer class="bgGradient text-white py-12 px-4 sm:px-6 lg:px-8">
        <div class="container mx-auto">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Company Info -->
                <div class="space-y-6">
                    <div>
                        <h3 class="text-2xl font-bold mb-4">A Curated Vacation
                        </h3>
                        <p class="text-gray-300 leading-relaxed">
                            The perfect headquarters for your Smoky Mountain Vacation! Nestled in the Spur of
                            Gatlinburg.
                        </p>
                    </div>

                    <div class="flex items-center text-gray-300">
                        <Icon name="lucide:map-marker" width="20" height="name" lucide="text-orange-500 mr-3" />
                        <span>Gatlinburg, Tennessee</span>
                    </div>
                </div>

                <!-- Links -->
                <div class="space-y-6">
                    <h4 class="text-xl font-semibold">Links</h4>
                    <ul class="space-y-3">
                        <li>
                            <a href="#" class="text-gray-300 hover:textColor transition-colors">
                                Home
                            </a>
                        </li>
                        <li>
                            <a href="#" class="text-gray-300 hover:textColor transition-colors">
                                About Us
                            </a>
                        </li>
                        <li>
                            <a href="#" class="text-gray-300 hover:textColor transition-colors">
                                About Owner

                            </a>
                        </li>
                        <li>
                            <a href="#" class="text-gray-300 hover:textColor transition-colors">
                                Vacation Rentals
                            </a>
                        </li>
                        <li>
                            <a href="#" class="text-gray-300 hover:textColor transition-colors">
                                Attractions
                            </a>
                        </li>
                        <li>
                            <a href="#" class="text-gray-300 hover:textColor transition-colors">
                                FAQ
                            </a>
                        </li>
                        <li>
                            <a href="#" class="text-gray-300 hover:textColor transition-colors">
                                Contact Us
                            </a>
                        </li>
                    </ul>
                </div>

                <!-- Contact -->
                <div class="space-y-6">
                    <h4 class="text-xl font-semibold">Contact</h4>
                    <div class="space-y-4">

                        <div class="flex items-center">
                            <Icon name="lucide:phone" width="20" height="name" class="text-gray-300 !size-4 mr-3" />
                            <span class="text-gray-300">(513) 314-7544</span>
                        </div>

                        <div class="flex items-center">
                            <Icon name="lucide:mail" width="20" height="name" class="text-gray-300 !size-4 mr-3" />
                            <span class="text-gray-300">acuratedvacation@gmail.com</span>
                        </div>
                        <div class="flex space-x-6">
                            <a href="#" class="text-gray-300 hover:text-orange-500 transition-colors">
                                <Icon name="lucide:facebook" class="text-gray-300 !size-4 mr-3" width="24" height="24" />
                            </a>
                            <a href="#" class="text-gray-300 hover:text-orange-500 transition-colors">
                                <Icon name="lucide:instagram" class="text-gray-300 !size-4 mr-3" width="24" height="24" />
                            </a>

                            <a href="#" class="text-gray-300 hover:text-orange-500 transition-colors">
                                <img src="/video.png" alt="" class="w-6 h-6">
                            </a>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Bottom Section -->
            <div class="border-t border-[#0b3a55] mt-12 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <p class="text-gray-300 text-sm mb-4 md:mb-0">
                        © {{ new Date().getFullYear() }} A Curated Vacation. All rights reserved.
                    </p>

                    <div class="flex items-center space-x-4">
                        <button
                            class="bgGradient text-white px-6 py-2 rounded-full font-medium transition-colors inline-flex items-center">
                            <Icon name="lucide:calendar" height="16" class="mr-2" />
                            Book Now
                        </button>
                    </div>
                </div>
            </div>

            <!-- Social Media Links -->

        </div>
    </footer>
</template>