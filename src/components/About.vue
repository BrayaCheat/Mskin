<template>
    <section id="about" class="bg-gray-50">
        <div class="flex flex-col justify-center items-center gap-6 pt-20 md:px-0 px-10 md:text-justify text-center">
            <h1 class="text-black font-bold text-4xl">Real Time, Forecasted, Future, Marine and Historical Weather</h1>
            <h1 class="text-zinc-500 font-medium text-xl">Free Weather Forecast in JSON and XML for commercial and
                non-commercial use</h1>
        </div>
        <div class="container mx-auto md:p-36 p-10 grid md:grid-cols-3 grid-cols-1 place-items-center gap-12">
            <div class="max-w-sm p-6 rounded-lg shadow-lg border-zinc-200 border">
                <img src="../assets/Images/about.jpg" alt="" class="w-full rounded-full p-10">
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
        <div class="container mx-auto md:px-36 p-10 grid md:grid-cols-2 grid-cols-1 gap-12">
            <div class="grid place-items-center" v-for="(img, index) in images" :key="img.id">
                <img v-if="img.show" :src="img.src" :alt="img.alt" class="rounded-lg w-full h-96 object-cover shadow-md duration-500" data-aos-duration="2000">
                <button v-if="!img.show" @click="showImages(index)" class="px-10 py-4 w-full bg-pink-300 rounded text-white hover:bg-pink-400 duration-500 shadow-md">
                    1. Click the button to see the images
                </button>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'About',
    data() {
        return {
            images: [
                { id: 1, src: 'src/assets/Images/img1.jpg', alt: 'img1', show: true, title: "1. Click the button to see the images" },
                { id: 2, src: 'src/assets/Images/img2.jpg', alt: 'img2', show: false, title: "2. Click the button to see the images" },
            ]
        }
    },
    methods: {
        showImages: function(index) {
            this.images = this.images.map((img, imgIndex) => {
                img.show = imgIndex == index;
                return img;
            })
        }
    }
}
</script>
