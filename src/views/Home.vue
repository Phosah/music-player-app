<template>
  <main class="my-20 flex">
    <div>
      <Sidebar />
    </div>
    <div class="w-2/3 flex-1 flex space-x-6 px-6">
      <div class="bg-green-200">
        <Banner />
        <div>
          <NewSongRelease :songs="songReleaseArr" />
        </div>
      </div>
    </div>
    <div class="w-1/3 bg-yellow-200"></div>
  </main>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import Sidebar from "../components/Sidebar.vue";
import Banner from "../components/Banner.vue";
import NewSongRelease from "../components/NewSongRelease.vue";
import type LatestSongRelease from "../types/LatestSongRelease";
import img1 from "@/assets/new-release-1.png";
import img2 from "@/assets/new-release-2.png";
import img3 from "@/assets/new-release-3.png";
import img4 from "@/assets/new-release-4.png";

export default defineComponent({
  name: "Home",
  components: { Sidebar, Banner, NewSongRelease },

  setup() {
    const songReleaseArr = ref<LatestSongRelease[]>([
      {
        img: img1,
        alt: "Taylor swift",
        title: "Red (Taylor’s Version)",
        artiste: "Taylor Swift"
      },
      {
        img: img2,
        alt: "Dojo Cat",
        title: "Need to Know",
        artiste: "Dojo Cat"
      },
      {
        img: img3,
        alt: "The weekend",
        title: "After Hours",
        artiste: "The Weekend"
      },
      {
        img: img4,
        alt: "Soundwave",
        title: "Hit Machine",
        artiste: "Soundwave"
      },
      {
        img: img1,
        alt: "Taylor swift",
        title: "Red (Taylor’s Version)",
        artiste: "Taylor Swift"
      },
    ])

    return { songReleaseArr }
  }
})
</script>
