<template>
    <div class="w-full h-80 relative rounded-md">
        <img
            class="h-full w-full absolute inset-0 object-cover rounded-md"
            src="@/assets/banner-photo.png"
            alt="Banner photo"
        />
        <SearchBar />
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
