<template>
    <section class="text-center py-14">
        <!-- Followers Count (Transparent background) -->
        <div class="inline-flex items-center bg-transparent px-3 rounded-full mb-4 border border-solid"> <span
                class="text-gradient font-bold">30,000+</span>
            <span class="ml-2">người tin dùng</span>
            <div class="ml-2 flex items-center -space-x-4">
                <img class="small-icon rounded-full" src="/assets/images/img1.svg" alt="">
                <img class="rounded-full " src="/assets/images/img2.svg" alt="">
                <img class=" rounded-full " src="/assets/images/img3.svg" alt="">
                <img class=" rounded-full" src="/assets/images/img4.svg" alt="">

            </div>
        </div>

        <!-- Main Heading with Gradient Text -->
        <h1 class=" font-bold text-3xl leading-[2.5rem] lg:text-6xl lg:leading-[4.5rem]">
            Giải pháp thiết kế <br>
            <span class="text-blue-gradient">
                Logo & Brand Identity <br>
                chuyên nghiệp
            </span>
        </h1>

        <!-- Subtext -->
        <p class="text-lg font-normal mt-6">Thu hút khách hàng ngay từ cái nhìn đầu tiên</p>

        <!-- Call to Action Button with Arrow Icon -->
        <a href="#"
            class="button-gradient mt-8 py-3 mx-auto px-6 text-white text-lg font-semibold rounded-full hover:shadow-lg w-[300px]  flex items-center justify-center">
            Nhận tư vấn miễn phí
            <!-- Arrow Icon -->
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"
                class="w-5 h-5 ml-2">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
            </svg>
        </a>

        <!-- banner | video  -->
        <div class="flex justify-center">
            <img src="/assets/images/banner.svg" alt="">
        </div>
    </section>
</template>

<style>
.button-gradient {
    @apply bg-gradient-to-r from-blue-gradient to-purple-gradient;
}

.text-gradient {
    @apply bg-gradient-to-r from-blue-gradient to-purple-gradient inline-block text-transparent bg-clip-text;
}
</style>