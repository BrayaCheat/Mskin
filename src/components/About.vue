<template>
    <section id="about">

        <div
            class="container mx-auto md:p-36 p-10 grid xl:grid-cols-3 lg:grid-cols-3 md:grid-cols-1 grid-cols-1 place-items-center gap-12">
            <div class="grid col-span-3 xl:px-0 px-10 gap-10 sm:py-0 pt-10 text-center">
                <h1 class="text-black font-bold text-4xl">Shops by categories</h1>
                <h1 class="text-zinc-500 font-medium text-xl">Free Weather Forecast in JSON and XML for commercial and
                    non-commercial use</h1>
            </div>
            <div class="grid col-span-3 xl:grid-cols-3 lg:grid-cols-2 md:grid-cols-1 place-items-center gap-10">
                <div class="max-w-sm p-6 rounded-lg shadow-lg border-zinc-200 border">
                <img src="../assets/Images/about.jpg" alt="" class="w-full rounded-full p-10">
                <h1 class="font-medium text-xl">1. SKINCARE</h1>
                <a href="#">
                    <h5 class="mb-2 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white">1.Title</h5>

                </a>
                <p class="mb-3 font-normal text-gray-500 dark:text-gray-400">Go to this step by step guideline process on
                    how to certify for your weekly benefits:</p>
                <a href="#" class="inline-flex items-center text-blue-600 hover:underline">
                    See our guideline
                    <svg class="w-3 h-3 ms-2.5 rtl:rotate-[270deg]" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                        fill="none" viewBox="0 0 18 18">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M15 11v4.833A1.166 1.166 0 0 1 13.833 17H2.167A1.167 1.167 0 0 1 1 15.833V4.167A1.166 1.166 0 0 1 2.167 3h4.618m4.447-2H17v5.768M9.111 8.889l7.778-7.778" />
                    </svg>
                </a>
            </div>
            <div class="max-w-sm p-6 rounded-lg shadow-lg border-zinc-200 border">
                <img src="../assets/Images/about.jpg" alt="" class="w-full rounded-full p-10">
                <h1 class="font-medium text-xl">2. HAIR</h1>
                <a href="#">
                    <h5 class="mb-2 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white">1.Title</h5>

                </a>
                <p class="mb-3 font-normal text-gray-500 dark:text-gray-400">Go to this step by step guideline process on
                    how to certify for your weekly benefits:</p>
                <a href="#" class="inline-flex items-center text-blue-600 hover:underline">
                    See our guideline
                    <svg class="w-3 h-3 ms-2.5 rtl:rotate-[270deg]" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                        fill="none" viewBox="0 0 18 18">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M15 11v4.833A1.166 1.166 0 0 1 13.833 17H2.167A1.167 1.167 0 0 1 1 15.833V4.167A1.166 1.166 0 0 1 2.167 3h4.618m4.447-2H17v5.768M9.111 8.889l7.778-7.778" />
                    </svg>
                </a>
            </div>
            <div class="max-w-sm p-6 rounded-lg shadow-lg border-zinc-200 border">
                <img src="../assets/Images/about.jpg" alt="" class="w-full rounded-full p-10">
                <h1 class="font-medium text-xl">3. MAKEUP</h1>
                <a href="#">
                    <h5 class="mb-2 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white">1.Title</h5>

                </a>
                <p class="mb-3 font-normal text-gray-500 dark:text-gray-400">Go to this step by step guideline process on
                    how to certify for your weekly benefits:</p>
                <a href="#" class="inline-flex items-center text-blue-600 hover:underline">
                    See our guideline
                    <svg class="w-3 h-3 ms-2.5 rtl:rotate-[270deg]" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                        fill="none" viewBox="0 0 18 18">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M15 11v4.833A1.166 1.166 0 0 1 13.833 17H2.167A1.167 1.167 0 0 1 1 15.833V4.167A1.166 1.166 0 0 1 2.167 3h4.618m4.447-2H17v5.768M9.111 8.889l7.778-7.778" />
                    </svg>
                </a>
            </div>
            </div>
            
            <div class="grid col-span-3">
                <a href=""><span class="text-pink-400 font-medium text-xl hover:underline hover:text-pink-500">View all
                        categories</span></a>
            </div>
        </div>


        <div class="container mx-auto lg:px-36 md:px-28 p-10 grid md:grid-cols-3 grid-cols-1 gap-12">
            <div class="relative md:col-span-2">
                <img v-for="img in images" :key="img.src" :src="img.src" :alt="img.alt" id="img"
                    class="img-animate transition-opacity rounded-lg object-cover shadow-md duration-500 border border-zinc-200"
                    :class="img.active ? '' : 'opacity-0'" data-aos-duration="2000">
            </div>
            <div class="flex flex-col items-center justify-center gap-10" id="btn">
                <button @click="showImages(index)" v-for="(btn, index) in buttons" :key="btn.id"
                    class="px-10 py-4 w-full bg-pink-300 rounded text-white hover:bg-pink-400 duration-500 shadow-md">
                    {{ btn.name }}
                </button>
            </div>
        </div>

    </section>
</template>

<script>
export default {
    data() {
        return {
            images: [
                { src: 'src/assets/Images/img1.jpg', alt: 'Image 1', active: true },
                { src: 'src/assets/Images/img2.jpg', alt: 'Image 2', active: false },
                { src: 'src/assets/Images/main-banner.jpg', alt: 'Image 3', active: false },
                { src: 'src/assets/Images/mainBanner.jpg', alt: 'Image 4', active: false },
            ],
            buttons: [
                { id: 1, name: 'Button 1' },
                { id: 2, name: 'Button 2' },
                { id: 3, name: 'Button 3' },
                { id: 4, name: 'Button 4' }
            ]
        }
    },
    methods: {
        showImages: function (index) {
            this.images = this.images.map((img, imgIndex) => {
                img.active = imgIndex == index;
                return img;
            })
        }
    },
}
</script>

<style scoped>
.img-animate {
    position: absolute;
    height: 100%;
    width: 100%;
}
</style>
