<template>
    <div class="mt-6">
        <div class="flex items-center justify-between">
            <p>You May Like</p>
            <p>See more</p>
        </div>
        <div class="grid grid-cols-7 gap-4">
            <div v-for="(song, ix) in songs" :key="ix">
                <div>
                    <img :src="song.img" :alt="song.alt" />
                    <p>{{ song.title }}</p>
                    <p>{{ song.artiste }}</p>
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
