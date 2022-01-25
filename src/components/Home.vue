<template>
  <div id="home">
    <img
      src="https://www.gravatar.com/avatar/ac9998c597a87af978beb083443f8eb7?s=800"
      alt="Me"
      class="profile-image"
    >

    <h1 class="text-white">Ricky Hu</h1>
    <h4 class="text-white">Learn more to contribute more.</h4>
    <h4 class="text-white">Programming / Speedcubing / Table Tennis / Cats</h4>
  </div>
</template>

<script lang="ts">
import {defineComponent} from "vue";

export default defineComponent({
  name: "Home",
  setup() {

  }
});
</script>

<style scoped>
.profile-image {
  @apply rounded-full w-32 md:w-48 lg:w-60;
}
</style>