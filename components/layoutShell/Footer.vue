<template>
    <footer class="bgGradient text-white py-12 px-4 sm:px-6 lg:px-8">
        <div class="container mx-auto">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Company Info -->
                <div class="space-y-6">
                    <div>
                        <img src="/A_Curated_Vacation_logo_page-0001__1_-removebg-preview.png" class="h-24" alt="">
                    </div>
                    <div>
                        <h3 class="text-2xl font-bold mb-4">A Curated Vacation
                        </h3>
                        <p class="text-gray-300 leading-relaxed">
                            Your Ultimate Inlet Beach Escape — Thoughtfully Curated for Relaxation, Comfort, and
                            Unforgettable Moments by the Sea
                        </p>
                    </div>

                    <div class="flex items-center space-x-2 text-gray-300">
                        <Icon name="lucide:map-pin" lucide="!size-6" />
                        <span> Inlet Beach, FL </span>
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
                                Property
                            </a>
                        </li>
                        <li>
                            <a href="#" class="text-gray-300 hover:textColor transition-colors">
                                Reviews
                            </a>
                        </li>
                        <li>
                            <a href="#" class="text-gray-300 hover:textColor transition-colors">
                                FAQ
                            </a>
                        </li>
                        <li>
                            <a href="#" class="text-gray-300 hover:textColor transition-colors">
                                Blogs
                            </a>
                        </li>
                        <li>
                            <a href="#" class="text-gray-300 hover:textColor transition-colors">
                                Contact
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
                                <Icon name="lucide:facebook" class="text-gray-300 !size-4 mr-3" width="24"
                                    height="24" />
                            </a>
                            <a href="#" class="text-gray-300 hover:text-orange-500 transition-colors">
                                <Icon name="lucide:instagram" class="text-gray-300 !size-4 mr-3" width="24"
                                    height="24" />
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
                            class="bgGradient hover:bg-[#5790a1] hover:scale-110 duration-300 text-white px-6 py-2 rounded-full font-medium transition-colors inline-flex items-center">
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