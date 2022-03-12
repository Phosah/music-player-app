<template>
  <div class="max-w-[90rem] mx-auto font-euclid-regular">
    <main>
      <router-view></router-view>
    </main>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({

})
</script>

<style>
@font-face {
  font-family: "Euclid Circular A";
  font-weight: 300;
  src: local("Euclid Circular A"),
    url("./fonts/Euclid-Circular-A-Light.ttf") format("OpenType");
}
@font-face {
  font-family: "Euclid Circular A";
  font-weight: 400;
  src: local("Euclid Circular A"),
    url("./fonts/Euclid-Circular-A-Regular.ttf") format("OpenType");
}
@font-face {
  font-family: "Euclid Circular A";
  font-weight: 500;
  src: local("Euclid Circular A"),
    url("./fonts/Euclid-Circular-A-Medium.ttf") format("OpenType");
}
@font-face {
  font-family: "Euclid Circular A";
  font-weight: 600;
  src: local("Euclid Circular A"),
    url("./fonts/Euclid-Circular-A-Semibold.ttf") format("OpenType");
}
@font-face {
  font-family: "Euclid Circular A";
  font-weight: 700;
  src: local("Euclid Circular A"),
    url("./fonts/Euclid-Circular-A-Bold.ttf") format("OpenType");
}

.font-euclid-light {
  font-family: "Euclid Circular A", sans-serif;
  font-weight: 300;
}
.font-euclid-regular {
  font-family: "Euclid Circular A", sans-serif;
  font-weight: 400;
}
.font-euclid-medium {
  font-family: "Euclid Circular A", sans-serif;
  font-weight: 500;
}
.font-euclid-semibold {
  font-family: "Euclid Circular A", sans-serif;
  font-weight: 600;
}
.font-euclid-bold {
  font-family: "Euclid Circular A", sans-serif;
  font-weight: 700;
}
</style>