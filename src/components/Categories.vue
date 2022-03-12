<template>
    <div class="mb-4">
        <div class="flex items-center justify-between mb-4">
            <h2 class="text-lg font-euclid-semibold">Categories</h2>
            <p class="text-[#F3777D]">See all</p>
        </div>
        <div class="grid grid-cols-2 gap-x-3 gap-y-2">
            <div class="h-16 relative rounded-sm" v-for="(category, ix) in categories" :key="ix">
                <img
                    class="absolute inset-0 object-cover h-full w-full rounded-sm"
                    :src="category.img"
                    :alt="category.alt"
                />
                <div class="flex items-center justify-center h-full">
                    <p class="text-lg text-white font-euclid-semibold z-50">{{ category.name }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import type Category from "@/types/Categories"
import type { PropType } from 'vue'

export default defineComponent({
    name: "Categories",
    props: {
        categories: {
            type: Array as PropType<Category[]>,
            required: true
        },
    },
    setup(props) {

    },
})
</script>
