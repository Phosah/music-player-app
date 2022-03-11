<template>
  <main class="my-20">
    <div class="flex">
      <div>
        <Sidebar />
      </div>
      <div class="w-2/3 flex-1 flex space-x-6 px-6">
        <div class="bg-green-200">
          <Banner />
          <div>
            <NewSongRelease :songs="songReleaseArr" />
            <SongsYouMayLike :songs="songsYouMayLikeArr" />
            <RecentlyPlayedSongs :recentlyPlayedSongs="playedSongsArr" />
          </div>
        </div>
      </div>
      <div class="w-1/3 bg-yellow-200">
        <TopStreams :streams="topStreamsArr" />
        <Categories :categories="categoriesArr" />
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
import img1 from "@/assets/new-release-1.png";
import img2 from "@/assets/new-release-2.png";
import img3 from "@/assets/new-release-3.png";
import img4 from "@/assets/new-release-4.png";
import img5 from "@/assets/top-streams-1.png";
import img6 from "@/assets/top-streams-2.png";
import img7 from "@/assets/top-streams-3.png";
import img8 from "@/assets/top-streams-4.png";
import img9 from "@/assets/top-streams-5.png";
import img10 from "@/assets/top-streams-6.png";
import img11 from "@/assets/top-streams-7.png";
import img12 from "@/assets/like-1.png"
import img13 from "@/assets/like-2.png"
import img14 from "@/assets/like-3.png"
import img15 from "@/assets/like-4.png"
import img16 from "@/assets/like-5.png"
import img17 from "@/assets/like-6.png"
import img18 from "@/assets/like-7.png"
import pop from "@/assets/category-1.png";
import jazz from "@/assets/category-2.png";
import romance from "../assets/category-3.png";
import chill from "@/assets/category-4.png";
import hiphop from "@/assets/category-5.png";
import rock from "@/assets/category-6.png";
import img20 from "../assets/recently-played-1.png"
import img21 from "../assets/recently-played-2.png"
import Categories from "../components/Categories.vue";
import type Category from "@/types/Categories";
import SongsYouMayLike from "../components/SongsYouMayLike.vue";
import type SongsToLike from "@/types/SongsToLike";
import RecentlyPlayedSongs from "../components/RecentlyPlayedSongs.vue";
import type { PropType } from "vue";
import type RecentlyPlayed from "@/types/RecentlyPlayed";
import NowPlaying from "../components/NowPlaying.vue";

export default defineComponent({
  name: "Home",
  components: { Sidebar, Banner, NewSongRelease, TopStreams, Categories, SongsYouMayLike, RecentlyPlayedSongs, NowPlaying },

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
    const topStreamsArr = ref<Streams[]>([
      {
        img: img8,
        alt: "Justin bieber",
        title: "Mistletoe",
        artiste: "Justin Bieber",
        duration: "3:45",
      },
      {
        img: img6,
        alt: "Adele",
        title: "Easy on me",
        artiste: "Adele",
        duration: "3:45",
      },
      {
        img: img7,
        alt: "Public Library Community",
        title: "Moonlight",
        artiste: "Public Library Commu...",
        duration: "3:45",
      },
      {
        img: img8,
        alt: "Taylor swift",
        title: "Red (Taylor’s Version)",
        artiste: "Taylor Swift",
        duration: "3:45",
      },
      {
        img: img9,
        alt: "88rising",
        title: "Midsummer Madness",
        artiste: "88rising",
        duration: "3:45",
      },
      {
        img: img10,
        alt: "Pink Sweat$",
        title: "I feel good",
        artiste: "Pink Sweat$",
        duration: "3:45",
      },
      {
        img: img11,
        alt: "Vincent Fable",
        title: "Get lost",
        artiste: "Vincent Fable",
        duration: "3:45",
      },
    ])
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
    const songsYouMayLikeArr = ref<SongsToLike[]>([
      {
        img: img12,
        alt: "Shaun",
        title: "Way Back Home",
        artiste: "Shaun",
      },
      {
        img: img18,
        alt: "The Clean Bandit",
        title: "Rockabye",
        artiste: "The Clean Bandit",
      },
      {
        img: img13,
        alt: "Pink Sweat$",
        title: "All my worst",
        artiste: "Pink Sweat$",
      },
      {
        img: img17,
        alt: "Kanye West",
        title: "Graduation",
        artiste: "Kanye West",
      },
      {
        img: img16,
        alt: "Zedd",
        title: "Stay",
        artiste: "Zedd",
      },
      {
        img: img15,
        alt: "Gayle",
        title: "abcdefu",
        artiste: "Gayle",
      },
      {
        img: img14,
        alt: "Ed Sheeran",
        title: "Bad Habits",
        artiste: "Ed Sheeran",
      },

    ])
    const playedSongsArr = ref<RecentlyPlayed[]>([
      {
        img: img20,
        alt: "Maria Carey",
        title: "All I Want For Christmas Is You",
        artiste: "Maria Carey",
        album: "Album",
        duration: "3:45"
      },
      {
        img: img21,
        alt: "Rose",
        title: "On The Ground",
        artiste: "Rose",
        album: "-R-",
        duration: "3:45"
      },

    ])
    return { songReleaseArr, topStreamsArr, categoriesArr, songsYouMayLikeArr, playedSongsArr }
  }
})
</script>
