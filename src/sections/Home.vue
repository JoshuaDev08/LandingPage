<template>
    <section class="relative h-screen overflow-hidden">
      <!-- Parallax background div -->
      <div
        ref="parallaxSection"
        class="absolute inset-0 bg-[url('/src/assets/background.jpg')] bg-cover bg-center"
        style="will-change: transform;"
      ></div>
  
      <!-- Overlay -->
      <div class="absolute inset-0 bg-black/60"></div>
  
      <!-- Navbar -->
      <div class="absolute top-0 left-0 w-full z-20">
        <Navbar />
      </div>
  
      <!-- Centered Content -->
      <div class="relative z-10 flex flex-col items-center justify-center h-full w-full text-white px-4">
        <p class="text-3xl md:text-5xl lg:text-7xl leading-tight max-w-full md:max-w-2xl lg:w-[800px] text-center font-serif">
          MAKE EVERY EVENT
          <span class="glow-text">UNFORGETTABLE</span> WITH OUR PHOTO BOOTH
        </p>
  
        <p class="font-serif text-sm md:text-lg mt-2">Private and Corporate Events</p>
  
        <SocialMediaList />
  
        <p class="font-serif text-xs md:text-base text-center mt-2">
          Fun and instant memories for weddings, birthdays, and corporate events
        </p>
  
        <div class="absolute bottom-0 mb-2 flex flex-col items-center">
          <p class="font-serif">Scroll Down</p>
          <GlassContainer width="40px" height="55px" rounded="100px">
            <div class="flex items-center justify-center h-full w-full">
              <font-awesome-icon icon="arrow-down" class="text-white text-xl animate-bounce" />
            </div>
          </GlassContainer>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import Navbar from '../components/Navbar.vue'
  import SocialMediaList from '../components/SocialMediaList.vue'
  import GlassContainer from '../components/GlassContainer.vue'
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
  import { ref, onMounted, onUnmounted } from 'vue'
  
  const parallaxSection = ref(null)
  let ticking = false
  
  const handleScroll = () => {
    if (!ticking) {
      window.requestAnimationFrame(() => {
        if (parallaxSection.value) {
          const offset = window.scrollY * 0.6 // slower movement
          parallaxSection.value.style.transform = `translateY(${offset}px)`
        }
        ticking = false
      })
      ticking = true
    }
  }
  
  onMounted(() => {
    window.addEventListener('scroll', handleScroll)
  })
  
  onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
  })
  </script>
  
  <style scoped>
  .glow-text {
    color: #FFFAC4;
    text-shadow: 0 0 5px #FFFAC4, 0 0 10px #FFFAC4;
    animation: glow-pulse 2s infinite alternate;
  }
  
  @keyframes glow-pulse {
    from {
      text-shadow: 0 0 3px #FFFAC4, 0 0 6px #FFFAC4;
    }
    to {
      text-shadow: 0 0 8px #FFFAC4, 0 0 16px #FFFAC4;
    }
  }
  </style>
  