<template>
    <div>
        <div class="flex items-center justify-between mb-4">
            <h3 class="font-semibold">Categories</h3>
            <p class="text-[#F3777D]">See all</p>
        </div>
        <div class="grid grid-cols-2 gap-x-3">
            <div v-for="(category, ix) in categories" :key="ix">
                <div class="relative h-24 rounded-md">
                    <img class="absolute inset-0" :src="category.img" :alt="category.alt" />
                    <div class="flex items-center justify-center">
                        <p class="text-white z-50">{{ category.name }}</p>
                    </div>
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
