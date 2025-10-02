<script setup>
import GlassContainer from './GlassContainer.vue';

</script>
<template>
    <GlassContainer width="200px" height="50px">
        <div class="flex items-center flex-row w-full h-full justify-center rounded-sm gap-3">
            <a class="tooltip tooltip-top rounded-sm" data-tip="Instagram">
                <img src="../assets/instagram.png" class="cursor-pointer" width="35px" alt="instagram">
            </a>
            <a class="tooltip tooltip-top rounded-sm" data-tip="Facebook">
                <img src="../assets/facebook.png" class="cursor-pointer" width="35px" alt="facebook">
            </a>
            <a class="tooltip tooltip-top rounded-sm" data-tip="Gmail">
                <img src="../assets/gmail.png" class="cursor-pointer" width="35px" alt="gmail">
            </a>
            <a class="tooltip tooltip-top rounded-sm" data-tip="Tik-Tok">
                <img src="../assets/tik-tok.png" class="cursor-pointer" width="35px" alt="tiktok">
            </a>
        </div>
    </GlassContainer>
</template>
<style lang="">
    
</style>