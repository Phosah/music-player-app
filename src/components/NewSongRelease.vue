<template>
    <div class="mt-8">
        <div class="flex items-center justify-between mb-4">
            <div class="flex items-center space-x-2">
                <h2 class="text-lg font-euclid-semibold">New Releases</h2>
                <svg
                    class="w-6 h-6 text-[#EE4950]"
                    fill="currentColor"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path
                        fill-rule="evenodd"
                        d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z"
                        clip-rule="evenodd"
                    />
                </svg>
            </div>
            <p class="text-[#F3777D]">See more</p>
        </div>
        <div class="grid grid-cols-5 gap-x-3">
            <div v-for="(song, ix) in songs" :key="ix">
                <div class="cursor-pointer">
                    <img class="mb-2" :src="song.img" :alt="song.alt" />
                    <p class="text-[#E4E7E5] font-semibold">{{ song.title }}</p>
                    <p class="text-xs text-[#AFB6B2]">{{ song.artiste }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import type { PropType } from "vue"
import type LatestSongRelease from '@/types/LatestSongRelease'

export default defineComponent({
    props: {
        songs: {
            type: Array as PropType<LatestSongRelease[]>,
            required: true
        }
    },
    setup(props) {

    },
})
</script>
