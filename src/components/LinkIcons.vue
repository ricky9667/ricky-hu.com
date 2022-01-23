<template>
  <div id="link-icons" class="flex flex-row justify-center gap-1 md:gap-3">
    <a v-for="(link, index) in links" :key="index" :href="link.url" target="_blank" class="link-icon-animation">
      <img
        :src="link.image"
        :alt="link.name"
        class="link-icon-image"
      >
    </a>
  </div>
</template>

<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: "LinkIcons",
  setup() {
    const links = [
      {
        name: "Facebook",
        url: "https://www.facebook.com/ricky.hu.0110/",
        image: "https://play-lh.googleusercontent.com/ccWDU4A7fX1R24v-vvT480ySh26AYp97g1VrIB_FIdjRcuQB2JP2WdY7h_wVVAeSpg=s360"
      },
      {
        name: "Instagram",
        url: "https://www.instagram.com/ricky_hu_0110/",
        image: "https://play-lh.googleusercontent.com/h9jWMwqb-h9hjP4THqrJ50eIwPekjv7QPmTpA85gFQ10PjV02CoGAcYLLptqd19Sa1iJ=s360"
      },
      {
        name: "Github",
        url: "https://github.com/ricky9667/",
        image: "https://play-lh.googleusercontent.com/PCpXdqvUWfCW1mXhH1Y_98yBpgsWxuTSTofy3NGMo9yBTATDyzVkqU580bfSln50bFU=s360"
      },
      {
        name: "Telegram",
        url: "https://t.me/ricky9667/",
        image: "https://play-lh.googleusercontent.com/ZU9cSsyIJZo6Oy7HTHiEPwZg0m2Crep-d5ZrfajqtsH-qgUXSqKpNA2FpPDTn-7qA5Q=s360"
      },
      {
        name: "LinkedIn",
        url: "https://www.linkedin.com/in/ricky9667/",
        image: "https://play-lh.googleusercontent.com/kMofEFLjobZy_bCuaiDogzBcUT-dz3BBbOrIEjJ-hqOabjK8ieuevGe6wlTD15QzOqw=s360"
      },
      {
        name: "Twitter",
        url: "https://twitter.com/ricky9667/",
        image: "https://play-lh.googleusercontent.com/6YKvTYU0qunPIsv7BvlQTrIKqbczaG75-POrOlVRdXdHlWqj3grpRs-MkkK6GJrVqjs=s360"
      },
      {
        name: "WCA",
        url: "https://worldcubeassociation.org/persons/2015HUSH02",
        image: "https://www.worldcubeassociation.org/assets/WCA%20Logo%202020-dacb67d012ad8fdf646e78159e7fcac40d11dab6b3828e790b00fbf67e4dcb88.svg"
      }
    ];

    return { links };
  }
});
</script>

<style scoped>
.link-icon-animation {
  @apply transform hover:-translate-y-1 transition duration-150;
}

.link-icon-image {
  @apply w-8 sm:w-10 rounded-full;
}
</style>