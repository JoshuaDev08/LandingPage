<template>
    <div class="relative w-full h-[500px] sm:h-[600px] md:h-[800px] overflow-visible">
        <!-- Slanted card -->
        <div class="w-[280px] sm:w-[300px] md:w-[340px] max-w-full
                    h-full sm:h-[500px] md:h-[700px]
                    bg-white text-black z-[1000] rounded-sm shadow-md p-2
                    mx-auto sm:relative md:relative lg:absolute lg:top-[-100px] lg:left-[450px] lg:-translate-x-1/2
                    sm:rotate-[5deg] md:rotate-0 lg:rotate-[18deg] sm:origin-top-left md:origin-top-left lg:origin-top-left">
            <!-- Image frames -->
            <div class="mb-2 rounded-sm overflow-hidden h-1/4 sm:h-1/3 md:h-[200px]">
                <img src="../assets/frame1.jpg" class="w-full h-full object-cover" alt="Photo 1" />
            </div>
            <div class="mb-2 rounded-sm overflow-hidden h-1/4 sm:h-1/3 md:h-[200px]">
                <img src="../assets/frame2.jpg" class="w-full h-full object-cover" alt="Photo 2" />
            </div>
            <div class="mb-2 rounded-sm overflow-hidden h-1/4 sm:h-1/3 md:h-[200px]">
                <img src="../assets/frame3.jpg" class="w-full h-full object-cover" alt="Photo 3" />
            </div>

            <!-- Footer with date -->
            <div class="flex text-center flex-col items-center justify-center mt-2">
                <p class="font-serif uppercase text-xl">Magnified Memories</p>
                <p class="font-serif">{{ currentDate }}</p>
            </div>
        </div>
    </div>
</template>


  
<script setup>
import { ref, onMounted } from 'vue'

const currentDate = ref('')

// Function to get date in MM.DD.YYYY format
function getDate() {
    const d = new Date()
    const month = String(d.getMonth() + 1).padStart(2, '0')
    const day = String(d.getDate()).padStart(2, '0')
    const year = d.getFullYear()
    return `${month}.${day}.${year}`
}

// Function to calculate milliseconds until next midnight
function msUntilMidnight() {
    const now = new Date()
    const nextMidnight = new Date()
    nextMidnight.setHours(24, 0, 0, 0) // next day 00:00:00
    return nextMidnight - now
}

// Initialize currentDate and set a timer to update at midnight
onMounted(() => {
    currentDate.value = getDate()

    setTimeout(() => {
        currentDate.value = getDate()

        setInterval(() => {
            currentDate.value = getDate()
        }, 24 * 60 * 60 * 1000)
    }, msUntilMidnight())
})
</script>
  
<style></style>
  