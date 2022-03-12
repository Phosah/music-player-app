<template>
    <div class="w-full h-80 relative rounded-md">
        <img
            class="h-full w-full absolute inset-0 object-cover rounded-md"
            src="@/assets/banner-photo.png"
            alt="Banner photo"
        />
        <SearchBar />
        <div class="absolute inset-0 h-full">
            <div class="h-full flex items-end justify-between p-5 z-50 font-euclid-bold">
                <div>
                    <p class="mb-4 text-xs font-semibold">FEATURED SONGS</p>
                    <p class="text-xl font-euclid-light">Post Malone</p>
                    <p class="text-4xl font-semibold">Circles</p>
                </div>
                <div class="flex items-center space-x-4 text-[#AFB6B3]">
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
                            d="M5 12h.01M12 12h.01M19 12h.01M6 12a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0z"
                        />
                    </svg>
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
                    <button class="py-3 px-8 bg-[#EE4950] text-white rounded-md">Play</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import SearchBar from './SearchBar.vue'

export default defineComponent({
    setup() {
    },
    components: { SearchBar }
})
</script>
