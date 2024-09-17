<script setup>
import { ref } from 'vue';
const isMenuOpen = ref(false);

const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value;
};

const beforeEnter = (el) => {
    el.style.opacity = 0;
    el.style.transform = 'translateY(-100%)';
};

const enter = (el, done) => {
    el.style.transition = 'opacity 0.3s ease, transform 0.3s ease';
    el.style.opacity = 1;
    el.style.transform = 'translateY(0)';
    done();
};

const leave = (el, done) => {
    el.style.transition = 'opacity 0.3s ease, transform 0.3s ease';
    el.style.opacity = 0;
    el.style.transform = 'translateY(-100%)';
    done();
};

</script>
<template>
    <header class="flex justify-between items-center pt-8 ">
        <!-- Logo -->
        <div class="text-xl font-bold">
            <img src="/assets/images/logo.svg" alt="Brandie Logo">
        </div>
        <!-- Hamburger Menu (visible on mobile) -->
        <div class="md:hidden">
            <button @click="toggleMenu" id="menu-btn" class="focus:outline-none">
                <svg v-if="isMenuOpen" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor" class="w-8 h-8">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                </svg>
                <svg v-else xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"
                    class="w-8 h-8">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
                </svg>
            </button>
            <transition name="slide-down" @before-enter="beforeEnter" @enter="enter" @leave="leave">
                <nav v-if="isMenuOpen" id="mobile-menu"
                    class="absolute top-[5rem] right-0 flex flex-col w-[12rem] items-end space-y-4 py-4 pr-4 bg-white">
                    <a href="#" class="hover:text-black">Dịch vụ thiết kế</a>
                    <a href="#" class="hover:text-black">Dự án</a>
                    <a href="#" class="hover:text-black">Bảng giá</a>
                    <a href="#" class="hover:text-black">Về chúng tôi</a>
                    <a href="#"
                        class="py-2 px-4 bg-gradient-to-r from-purple-500 to-pink-500 text-white rounded-full hover:shadow-lg">Liên
                        hệ</a>
                </nav>
            </transition>
        </div>
        <!-- Navigation Links (Flex to the right) -->
        <nav class="hidden md:flex ml-auto space-x-8 items-center font-medium">
            <!-- "Dịch vụ thiết kế" with triangle down icon -->
            <a href="#" class="hover:text-black flex items-center">
                Dịch vụ thiết kế
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"
                    class="w-4 h-4 ml-1">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
            </a>
            <a href="#" class="hover:text-black">Dự án</a>
            <a href="#" class="hover:text-black">Bảng giá</a>
            <a href="#" class="hover:text-black">Về chúng tôi</a>
        </nav>
        <!-- Mobile Menu (visible on small screens when toggled) -->

        <!-- Contact Button -->
        <a href="#"
            class="hidden md:inline-block button-gradient ml-8 py-2 px-4 bg-gradient-to-r from-purple-500 to-pink-500 text-white rounded-full hover:shadow-lg">Liên
            hệ</a>
    </header>
</template>