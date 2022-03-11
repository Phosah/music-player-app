<template>
    <div class="mt-10">
        <div class="flex space-x-2 items-center mb-4">
            <p class="font-semibold">Recently played</p>
            <svg
                class="w-6 h-6 text-[#F3777D]"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
            >
                <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M10 9v6m4-6v6m7-3a9 9 0 11-18 0 9 9 0 0118 0z"
                />
            </svg>
        </div>
        <div v-for="(song, ix) in recentlyPlayedSongs" :key="ix">
            <div class="flex items-center justify-between space-x-4 mb-3 text-[#AFB6B2]">
                <div class="flex-1 flex items-center space-x-2">
                    <p>{{ ix }}</p>
                    <div>
                        <img :src="song.img" :alt="song.alt" />
                    </div>
                    <p class="flex-1">{{ song.title }}</p>
                </div>
                <div class="flex-1 flex justify-center">{{ song.artiste }}</div>
                <div class="flex-1 flex justify-center">{{ song.album }}</div>
                <div class="flex items-center space-x-2">
                    <p>{{ song.duration }}</p>
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
                            d="M4 8h16M4 16h16"
                        />
                    </svg>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import type { PropType } from 'vue'
import type RecentlyPlayed from '@/types/RecentlyPlayed'

export default defineComponent({
    name: "RecentlyPlayedSongs",
    props: {
        recentlyPlayedSongs: {
            type: Array as PropType<RecentlyPlayed[]>,
            required: true
        }
    },
    setup(props) {

    },
})
</script>
