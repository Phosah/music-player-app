<template>
    <div class="mt-10">
        <div class="flex items-center justify-between mb-4">
            <h2 class="text-lg font-euclid-semibold">You May Like</h2>
            <p class="text-[#F3777D]">See more</p>
        </div>
        <div class="grid grid-cols-7 gap-4">
            <div v-for="(song, ix) in songs" :key="ix">
                <div class="text-center">
                    <img class="mb-2 w-14 mx-auto h-14" :src="song.img" :alt="song.alt" />
                    <p class="font-euclid-semibold">{{ song.title }}</p>
                    <p class="text-xs text-[#AFB6B2]">{{ song.artiste }}</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
import type { PropType } from 'vue'
import type SongsToLike from '@/types/SongsToLike'

export default defineComponent({
    name: "SongsYouMayLike",
    props: {
        songs: {
            type: Array as PropType<SongsToLike[]>,
            required: true,
        }
    },

    setup(props) {

    },
})
</script>
