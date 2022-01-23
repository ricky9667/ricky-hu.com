<template>
  <div class="home">
    <img
      src="https://www.gravatar.com/avatar/ac9998c597a87af978beb083443f8eb7?s=800"
      alt="Me"
      class="profile-image"
    >

    <h1 class="text-white">Ricky Hu</h1>
    <h4 class="text-white">Programming / Speedcubing / Table Tennis / Cats</h4>
    <div class="flex flex-row justify-center gap-4">
      <img
        src="https://play-lh.googleusercontent.com/ccWDU4A7fX1R24v-vvT480ySh26AYp97g1VrIB_FIdjRcuQB2JP2WdY7h_wVVAeSpg=s360"
        alt="Facebook"
        class="link-icon"
      >
      <img
        src="https://play-lh.googleusercontent.com/h9jWMwqb-h9hjP4THqrJ50eIwPekjv7QPmTpA85gFQ10PjV02CoGAcYLLptqd19Sa1iJ=s360"
        alt="Instagram"
        class="link-icon"
      >
      <img
        src="https://play-lh.googleusercontent.com/ZU9cSsyIJZo6Oy7HTHiEPwZg0m2Crep-d5ZrfajqtsH-qgUXSqKpNA2FpPDTn-7qA5Q=s360"
        alt="Telegram"
        class="link-icon"
      >
      <img
        src="https://play-lh.googleusercontent.com/PCpXdqvUWfCW1mXhH1Y_98yBpgsWxuTSTofy3NGMo9yBTATDyzVkqU580bfSln50bFU=s360"
        alt="Github"
        class="link-icon"
      >
      <img
        src="https://play-lh.googleusercontent.com/kMofEFLjobZy_bCuaiDogzBcUT-dz3BBbOrIEjJ-hqOabjK8ieuevGe6wlTD15QzOqw=s360"
        alt="LinkedIn"
        class="link-icon"
      >
      <img
        src="https://play-lh.googleusercontent.com/6YKvTYU0qunPIsv7BvlQTrIKqbczaG75-POrOlVRdXdHlWqj3grpRs-MkkK6GJrVqjs=s360"
        alt="Twitter"
        class="link-icon"
      >
      <img
        src="https://www.worldcubeassociation.org/assets/WCA%20Logo%202020-dacb67d012ad8fdf646e78159e7fcac40d11dab6b3828e790b00fbf67e4dcb88.svg"
        alt="WCA"
        class="link-icon"
      >
    </div>
  </div>
</template>

<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: "Home",
});
</script>

<style scoped>
.home {
  height: 100vh;
  background-color: #2c3e50;
  //background-image: url("https://ik.imagekit.io/pxhytijjnsj/Temp/152530761_3648777875237713_503035110259364789_n_zXjswZWEz.jpg?ik-sdk-version=javascript-1.4.3&updatedAt=1642855775326");
  //background-position: center;
}

.profile-image {
  @apply rounded-full w-32 md:w-48 lg:w-60;
}

.link-icon {
  @apply w-10;
  @apply rounded-full;
}
</style>