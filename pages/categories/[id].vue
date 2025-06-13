<template>
    <div class="bg-gray-50">
        <div class=" px-4 py-8 lg:py-16">

            <!-- The Gauge Coffeehouse Section -->
            <div class="grid lg:grid-cols-2 gap-8 lg:gap-16 ">

                <!-- Image Section -->
                <div class="order-2 lg:order-1">
                    <div class="relative">
                        <img src="/categories/657a2829e5278.png"
                            alt="The Gauge Coffeehouse outdoor seating area with yellow umbrella, rustic blue building, stone patio, and wooden chairs"
                            class="w-full h-full rounded-lg shadow-lg fade-in-element">
                    </div>
                </div>

                <!-- Content Section -->
                <div class="order-1 lg:order-2 relative border border-gray-400 bg-white max-w-xl">

                    <!-- Dotted Pattern Background - positioned on the right side -->


                    <div class="relative pr-4 lg:pr-8 ">
                        <h1
                            class="text-3xl lg:text-3xl  font-bold text-[#1B7895] mb-6 lg:mb-8 leading-tight fade-in-element">
                            The Gauge Coffeehouse & Humble Pie
                        </h1>

                        <p
                            class="text-gray-700 text-base lg:text-lg leading-relaxed lg:leading-relaxed fade-in-element">
                            The Gauge Coffeehouse is a casual place to start your day. They offer
                            coffee drinks, homemade bagels and muffins. This is also the Chattooga
                            Whitewater Shop where you'll find river gear, clothing and information about
                            shuttle service to and from the river. Humble Pie Pizza is next door to The
                            Gauge. It's a great place to unwind after a day exploring the area.
                        </p>
                        <div class="absolute right-0">
                            <img src="public/categories/dot-shape.png" alt="">
                        </div>
                    </div>
                </div>

            </div>
        </div>

        <!-- Optional: Back to top button -->
        <div class="fixed bottom-6 right-6 z-50">
            <button @click="scrollToTop"
                class="bg-[#1B7895] hover:bg-[#5790a1] text-white p-3 rounded-full shadow-lg transition-all duration-300 hover:scale-110">
                <Icon name="mdi:arrow-up" class="text-xl" />
            </button>
        </div>
    </div>
</template>

<script setup>
import { useRoute } from 'nuxt/app';
import { onMounted, onBeforeUnmount } from 'vue';

// Get the route parameter
const route = useRoute();
const categoryId = route.params.id;

// Function to scroll to top
const scrollToTop = () => {
    window.scrollTo({ top: 0, behavior: 'smooth' });
};

// Animation handling
let observer;

onMounted(() => {
    // Add smooth scroll behavior
    document.documentElement.style.scrollBehavior = 'smooth';

    // Initialize intersection observer
    observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
            if (entry.isIntersecting) {
                entry.target.style.opacity = '1';
                entry.target.style.transform = 'translateY(0)';
            }
        });
    });

    // Apply animation to elements
    document.querySelectorAll('.fade-in-element').forEach((el) => {
        el.style.opacity = '0';
        el.style.transform = 'translateY(20px)';
        el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
        observer.observe(el);
    });
});

// Clean up the observer when component is unmounted
onBeforeUnmount(() => {
    if (observer) {
        observer.disconnect();
    }
});
</script>

<style scoped>
.dotted-pattern {
    background-image: url('/categories/dot-shape.png');
    background-size: contain;
    background-repeat: repeat;
}

.fade-in-element {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.6s ease, transform 0.6s ease;
}
</style>