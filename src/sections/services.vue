<template >
    <section class="relative w-full h-[900px] overflow-hidden flex">
        <BlurCircle width="600px" height="600px" color="#D070FF" opacity="0.8" top="1%" left="100%" />
        <BlurCircle width="200px" height="200px" color="#D070FF" opacity="0.9" top="100%" left="0%" />
        <!-- Left Container -->
        <div class="w-1/2 flex items-center justify-center px-8">
            <div class="text-white text-center md:text-left">
                <h1 class="text-4xl md:text-6xl text-black uppercase font-serif">Exceptional photo booth</h1>
                <p class="mt-4 text-sm md:text-lg text-black">
                    We make every event unforgettable with fun, interactive, and modern photo booth experiences. Whether
                    it’s a wedding, birthday, or corporate event, our booths are designed to capture smiles and create
                    lasting memories.
                </p>
                <div class="flex flex-row mt-2 items-end">
                    <div class="w-1/8 h-[100px] items-center flex justify-center">
                        <img src="../assets/right-drawn-arrow.png" alt="arrow" width="90%">
                    </div>
                    <div class="flex-1 flex">
                        <p class="font-serif text-black ml-2">Retro Photobooth – Classic vibes with a modern twist, perfect
                            for vintage-themed events.</p>
                    </div>
                </div>
                <div class="flex flex-row mt-2 items-end">
                    <div class="w-1/8 h-[100px] items-center flex justify-center">
                        <img src="../assets/right-drawn-arrow.png" alt="arrow" width="90%">
                    </div>
                    <div class="flex-1 flex">
                        <p class="font-serif text-black ml-2">Mirror Photobooth – Sleek, full-length mirror with interactive
                            touch screen and animations.</p>
                    </div>
                </div>
                <div class="flex flex-row mt-2 items-end">
                    <div class="w-1/8 h-[100px] items-center flex justify-center">
                        <img src="../assets/right-drawn-arrow.png" alt="arrow" width="90%">
                    </div>
                    <div class="flex-1 flex">
                        <p class="font-serif text-black ml-2">Enclosed Photobooth – Private, cozy setup for groups who love
                            fun without the crowd.</p>
                    </div>
                </div>
                <div class="flex flex-row mt-2 items-end">
                    <div class="w-1/8 h-[100px] items-center flex justify-center">
                        <img src="../assets/right-drawn-arrow.png" alt="arrow" width="90%">
                    </div>
                    <div class="flex-1 flex">
                        <p class="font-serif text-black ml-2">Video & Audio Guestbook – Let your guests record heartfelt
                            messages, creating a memorable keepsake.</p>
                    </div>
                </div>
                <div class="mt-6">
                    <a class="btn btn-neutral font-alt rounded-sm text-white">Book Now</a>
                </div>
            </div>
        </div>

        <!-- Right Container -->
        <div class="w-1/2 flex items-center justify-center px-8">
            <div class="text-white text-center md:text-left">
                <h1 class="text-4xl md:text-6xl font-bold uppercase">Hello</h1>
                <p class="mt-4 text-lg md:text-xl">
                    Some description or content for the right container. This can be your image, cards, or extra info.
                </p>
            </div>
        </div>
    </section>
</template>
<script setup>
import BlurCircle from '../components/blurryCircle.vue'
</script>
<style ></style>