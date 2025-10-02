<template>
    <!-- Drawer wrapper -->
    <div class="drawer drawer-end">
        <input id="my-drawer-4" type="checkbox" class="drawer-toggle" />

        <!-- Sticky Navbar (only drawer-content is sticky) -->
        <div class="drawer-content">
            <div class="sticky top-2 z-10 p-2">
                <nav class="navbar rounded-sm glass-tv-border" style="border-radius: 10px;">
                    <!-- Left (brand / logo) -->
                    <div class="navbar-start">
                        <div class="avatar cursor-pointer">
                            <div class="w-14 ml-0 lg:ml-4 rounded-full">
                                <img src="../assets/Logo.png" />
                            </div>
                        </div>
                        <div class="flex flex-col">
                            <a class="font-alt normal-case text-xl text-white ml-0 lg:ml-2">MAGNIFIED</a>
                            <a class="font-handwriting text-[#FFFAC4] text-xl ml-0 lg:ml-2">MEMORIES</a>
                        </div>
                    </div>

                    <!-- Center (links, hidden on mobile/tablet) -->
                    <div class="navbar-center hidden lg:flex">
                        <ul class="menu menu-horizontal px-1 text-white font-alt gap-2">
                            <li><a href="#home" class="text-lg">Home</a></li>
                            <li><a href="#services" class="text-lg">Services</a></li>
                            <li><a href="#gallery" class="text-lg">Gallery</a></li>
                            <li><a href="#faq" class="text-lg">FAQ</a></li>
                            <li><a href="#contact" class="text-lg">Contact</a></li>
                        </ul>
                    </div>

                    <!-- Right (actions) -->
                    <div class="navbar-end">
                        <!-- Show button only on desktop -->
                        <a class="btn btn-accent font-alt mr-2 rounded-md hidden lg:inline-flex">Book Now</a>

                        <!-- Drawer toggle button -->
                        <label for="my-drawer-4" class="btn btn-ghost text-white lg:hidden">
                            <font-awesome-icon icon="bars" class="text-2xl"/>
                        </label>
                    </div>
                </nav>
            </div>
        </div>

        <!-- Drawer side (works correctly now) -->
        <div class="drawer-side z-50">
            <label for="my-drawer-4" aria-label="close sidebar" class="drawer-overlay"></label>
            <ul class="menu bg-base-200 text-base-content min-h-full w-80 p-4">
                <li><a href="#home" @click="closeDrawer">Home</a></li>
                <li><a href="#services" @click="closeDrawer">Services</a></li>
                <li><a href="#gallery" @click="closeDrawer">Gallery</a></li>
                <li><a href="#faq" @click="closeDrawer">FAQ</a></li>
                <li><a href="#contact" @click="closeDrawer">Contact</a></li>
                <li><a class="btn btn-accent font-alt mt-2">Book Now</a></li>
            </ul>
        </div>
    </div>
</template>
<script setup>
const closeDrawer = () => {
    const drawer = document.getElementById("my-drawer-4")
    if (drawer) drawer.checked = false
}
</script>
  