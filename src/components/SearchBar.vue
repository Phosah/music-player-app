<template>
    <div class="relative z-50 pt-6">
        <div class="flex items-center justify-between w-96 mx-auto px-3 py-2 bg-white rounded-md">
            <div class="flex items-center space-x-2 w-full">
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
                        d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
                    />
                </svg>
                <input
                    class="w-full focus-within:outline-none"
                    type="text"
                    placeholder="Search artists, songs, albums..."
                />
            </div>
            <div class="pl-2 border-l-2 border-[#959D99]">
                <svg
                    class="w-6 h-6"
                    fill="currentColor"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path
                        fill-rule="evenodd"
                        d="M7 4a3 3 0 016 0v4a3 3 0 11-6 0V4zm4 10.93A7.001 7.001 0 0017 8a1 1 0 10-2 0A5 5 0 015 8a1 1 0 00-2 0 7.001 7.001 0 006 6.93V17H6a1 1 0 100 2h8a1 1 0 100-2h-3v-2.07z"
                        clip-rule="evenodd"
                    />
                </svg>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "SearchBar",
    setup() {

    },
})
</script>
