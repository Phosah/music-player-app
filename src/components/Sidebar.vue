<template>
    <div class="w-56 px-4 pt-6 bg-[#272727] border-r border-[#313533]">
        <div class="mb-12">
            <img class="w-28" src="../assets/logo.png" alt="Logo" />
        </div>
        <div class="mb-16 font-euclid-bold">
            <div class="flex items-center space-x-2 mb-5">
                <!-- <svg
                    class="w-6 h-6"
                    fill="currentColor"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path
                        d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"
                    />
                </svg>-->
                <svg
                    class="w-6 h-6"
                    fill="none"
                    stroke="currentColor"
                    viewBox="0 0 24 24"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
                    />
                </svg>
                <p>Home</p>
            </div>
            <div class="flex items-center space-x-2 mb-5">
                <svg
                    class="w-6 h-6"
                    fill="none"
                    stroke="currentColor"
                    viewBox="0 0 24 24"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"
                    />
                </svg>
                <p>Browse</p>
            </div>
            <div class="flex items-center space-x-2 mb-5">
                <svg
                    class="w-6 h-6"
                    fill="none"
                    stroke="currentColor"
                    viewBox="0 0 24 24"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"
                    />
                </svg>
                <p>Favorite</p>
            </div>
            <div class="flex items-center space-x-2 mb-5">
                <svg
                    width="24"
                    height="24"
                    viewBox="0 0 24 24"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path
                        d="M3.47375 18.0671V12.3445C3.47375 10.0679 4.37813 7.88452 5.98792 6.27473C7.59772 4.66493 9.78107 3.76056 12.0577 3.76056C14.3343 3.76056 16.5176 4.66493 18.1274 6.27473C19.7372 7.88452 20.6416 10.0679 20.6416 12.3445V18.0671"
                        stroke="white"
                        stroke-width="1.90754"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    />
                    <path
                        d="M20.6416 19.0208C20.6416 19.5267 20.4406 20.0119 20.0829 20.3697C19.7251 20.7274 19.2399 20.9284 18.734 20.9284H17.7803C17.2744 20.9284 16.7892 20.7274 16.4314 20.3697C16.0737 20.0119 15.8727 19.5267 15.8727 19.0208V16.1595C15.8727 15.6536 16.0737 15.1684 16.4314 14.8107C16.7892 14.453 17.2744 14.252 17.7803 14.252H20.6416V19.0208ZM3.47375 19.0208C3.47375 19.5267 3.67473 20.0119 4.03246 20.3697C4.39019 20.7274 4.87538 20.9284 5.38129 20.9284H6.33506C6.84097 20.9284 7.32616 20.7274 7.68389 20.3697C8.04162 20.0119 8.24259 19.5267 8.24259 19.0208V16.1595C8.24259 15.6536 8.04162 15.1684 7.68389 14.8107C7.32616 14.453 6.84097 14.252 6.33506 14.252H3.47375V19.0208Z"
                        stroke="white"
                        stroke-width="1.90754"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    />
                </svg>
                <p>Library</p>
            </div>
        </div>
        <div class="font-euclid-medium">
            <div class="flex items-center justify-between mb-3">
                <div class="flex items-center space-x-2 text-[#2E3A59]">
                    <svg
                        class="w-6 h-6"
                        fill="none"
                        stroke="currentColor"
                        viewBox="0 0 24 24"
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
                        />
                    </svg>
                    <p>Home</p>
                </div>
                <div>
                    <svg
                        class="w-6 h-6"
                        fill="none"
                        stroke="currentColor"
                        viewBox="0 0 24 24"
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            d="M12 9v3m0 0v3m0-3h3m-3 0H9m12 0a9 9 0 11-18 0 9 9 0 0118 0z"
                        />
                    </svg>
                </div>
            </div>
            <div class="flex items-center space-x-3 mb-4 text-[#F3777D]">
                <p>For workspace</p>
                <svg
                    width="20"
                    height="20"
                    viewBox="0 0 20 20"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path
                        d="M2.32361 7.68958H3.91322V17.2273H2.32361V7.68958ZM7.09245 2.92075H8.68206V17.2273H7.09245V2.92075ZM11.8613 10.074H13.4509V17.2273H11.8613V10.074ZM16.6301 5.30517H18.2197V17.2273H16.6301V5.30517Z"
                        fill="#F3777D"
                        stroke="#F3777D"
                        stroke-width="0.763014"
                    />
                </svg>
            </div>
            <div class="text-[#959D99]">
                <p class="mb-4">Rich Brian’s collections</p>
                <p class="mb-4">deep focus</p>
                <p class="mb-4">Lo-Fi Jazz upbeat</p>
                <p class="mb-4">For workplace</p>
                <p class="mb-4">Christmas playlist</p>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "Sidebar",
    setup() {

    },
})
</script>
