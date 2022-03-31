<template>
    <div class="p-3 mb-8 bg-[#1E1E1E] rounded-md">
        <div class="flex items-center justify-between mb-4">
            <h3 class="text-base font-euclid-semibold">Top Streams Real-time</h3>
            <div class="flex items-center p-1 bg-[#49504D] rounded-sm">
                <button class="px-2 py-1 bg-[#EE4950]">Local</button>
                <button class="px-2 py-1">Global</button>
            </div>
        </div>
        <div class="text-[#AFB6B2]" v-for="(stream, ix) in streams" :key="ix">
            <div class="flex items-center justify-between pb-3 border-b border-[#313533] mb-3">
                <div class="flex items-center space-x-2">
                    <p>{{ stream.id }}</p>
                    <img :src="stream.img" :alt="stream.alt" />
                    <div>
                        <p class="text-white font-euclid-semibold">{{ stream.title }}</p>
                        <p class="text-xs">{{ stream.artiste }}</p>
                    </div>
                </div>
                <div class="flex items-center space-x-2">
                    <p>{{ stream.duration }}</p>
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
                </div>
            </div>
        </div>
        <div class="flex space-x-2 items-center justify-center mt-8">
            <p>Expand</p>
            <svg
                class="w-4 h-4"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
            >
                <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M19 9l-7 7-7-7"
                />
            </svg>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import type { PropType } from 'vue'
import type Stream from "@/types/TopStreams"


export default defineComponent({
    name: "TopStreams",
    props: {
        streams: {
            type: Array as PropType<Stream[]>,
            required: true
        }
    },
    setup(props) {

    },
})
</script>
