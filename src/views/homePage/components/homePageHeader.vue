<template>
    <header class="flex justify-between items-center pt-8 px-8">
        <!-- Logo -->
        <div class="text-xl font-bold">
            <img src="/assets/images/logo.svg" alt="Brandie Logo" >
        </div>

        <!-- Navigation Links (Flex to the right) -->
        <nav class="ml-auto space-x-8 flex items-center font-medium">
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

        <!-- Contact Button -->
        <a href="#"
            class="button-gradient ml-8 py-2 px-4 bg-gradient-to-r from-purple-500 to-pink-500 text-white rounded-full hover:shadow-lg">Liên
            hệ</a>
    </header>
</template>