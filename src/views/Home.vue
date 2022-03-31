<template>
  <main class="text-sm text-[#FAFAFA]">
    <div class="flex">
      <div class="flex self-stretch">
        <Sidebar />
      </div>
      <div class="flex-1 flex space-x-6 px-6 pt-6 bg-[#171717]">
        <div class="w-4/6">
          <div class>
            <Banner />
            <div>
              <NewSongRelease :songs="newReleaseArray" />
              <SongsYouMayLike :songs="songsYouMayLikeArray" />
              <RecentlyPlayedSongs :recentlyPlayedSongs="recentlyPlayedSongsArr" />
            </div>
          </div>
        </div>
        <div class="w-2/6">
          <TopStreams :streams="topStreamsArray" />
          <Categories :categories="categoriesArr" />
        </div>
      </div>
    </div>
    <NowPlaying />
  </main>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import Sidebar from "../components/Sidebar.vue";
import Banner from "../components/Banner.vue";
import NewSongRelease from "../components/NewSongRelease.vue";
import type LatestSongRelease from "../types/LatestSongRelease";
import TopStreams from "../components/TopStreams.vue";
import type Streams from "@/types/TopStreams";
import pop from "@/assets/category-1.png";
import jazz from "@/assets/category-2.png";
import romance from "../assets/category-3.png";
import chill from "@/assets/category-4.png";
import hiphop from "@/assets/category-5.png";
import rock from "@/assets/category-6.png";
import Categories from "../components/Categories.vue";
import type Category from "@/types/Categories";
import SongsYouMayLike from "../components/SongsYouMayLike.vue";
import type SongsToLike from "@/types/SongsToLike";
import RecentlyPlayedSongs from "../components/RecentlyPlayedSongs.vue";
import type { PropType } from "vue";
import type RecentlyPlayed from "@/types/RecentlyPlayed";
import NowPlaying from "../components/NowPlaying.vue";
import AllSongs from "@/db.json"

export default defineComponent({
  name: "Home",
  components: { Sidebar, Banner, NewSongRelease, TopStreams, Categories, SongsYouMayLike, RecentlyPlayedSongs, NowPlaying },

  setup() {
    const categoriesArr = ref<Category[]>([
      {
        img: pop,
        alt: "Pop",
        name: "Pop"
      },
      {
        img: jazz,
        alt: "Jazz",
        name: "Jazz"
      },
      {
        img: pop,
        alt: "Rock",
        name: "Rock"
      },
      {
        img: jazz,
        alt: "Romance",
        name: "Romance"
      },
      {
        img: pop,
        alt: "Hiphop",
        name: "Hiphop"
      },
      {
        img: jazz,
        alt: "Chill",
        name: "Chill"
      },
    ])

    const topStreamsArray = ref<Streams[]>((AllSongs.topStreams))
    const newReleaseArray = ref<LatestSongRelease[]>(AllSongs.newRelease)
    const songsYouMayLikeArray = ref<SongsToLike[]>(AllSongs.songsYouMayLike)
    const recentlyPlayedSongsArr = ref<RecentlyPlayed[]>(AllSongs.recentlyPlayed)

    return { categoriesArr, topStreamsArray, newReleaseArray, songsYouMayLikeArray, recentlyPlayedSongsArr }
  }
})
</script>
