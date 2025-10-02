<template >
    <div class="relative w-full h-full md:h-[800px] sm:h-full">
        <div class="absolute inset-0 overflow-hidden z-0">
            <BlurCircle width="600px" height="600px" color="#D070FF" opacity="0.8" top="1%" left="100%" />
            <BlurCircle width="200px" height="200px" color="#D070FF" opacity="0.9" top="100%" left="0%" />
        </div>
        <section class="relative w-full h-full flex flex-col md:flex-row">
            <!-- Left Container -->
            <div class="w-full md:w-1/2 flex items-center justify-center px-2 md:px-10 py-2 md:py-0">
                <ServicesList />
            </div>

            <!-- Right Container -->
            <div class="w-full md:w-1/2 flex items-center justify-center px-4 md:px-8 overflow-visible py-6 md:py-0">
                <Framer />
            </div>
        </section>
    </div>
</template>
<script setup>
import BlurCircle from '../components/blurryCircle.vue'
import Framer from '../components/frame3by3.vue'
import ServicesList from '../components/ServicesList.vue'
</script>
<style ></style>