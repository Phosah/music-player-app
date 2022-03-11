<template>
    <div class="mt-4">
        <div class="flex items-center space-x-2 mb-4">
            <p>New Releases</p>
            <svg
                class="w-6 h-6"
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
        <div class="grid grid-cols-5 gap-x-3">
            <div v-for="(song, ix) in songs" :key="ix">
                <img class="mb-2" :src="song.img" :alt="song.alt" />
                <p class="mb-1">{{ song.title }}</p>
                <p>{{ song.artiste }}</p>
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
