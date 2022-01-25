<template>
  <div>
    <nav id="navbar" class="h-16 px-8 py-0">
      <a href="/">
        <h2 class="text-white float-left navbar-text">🇹🇼 Ricky Hu</h2>
      </a>
      <h2 class="text-white float-right navbar-text">About</h2>
    </nav>
    <Home class="my-8"/>
    <LinkIcons/>
  </div>
</template>

<script lang="ts">
import {defineComponent, onMounted} from "vue";
import Home from "./components/Home.vue";
import LinkIcons from "./components/LinkIcons.vue";

export default defineComponent({
  name: "App",
  components: {
    Home,
    LinkIcons,
  },
  setup() {
    onMounted(() => document.title = "Ricky Hu")
  }
});
</script>

<style>
html, body {
  margin: 0;
  padding: 0;
  height: 100vh;
  background-color: #2c3e50;
  background-image: url("data:image/svg+xml,%3Csvg width='64' height='64' viewBox='0 0 64 64' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M8 16c4.418 0 8-3.582 8-8s-3.582-8-8-8-8 3.582-8 8 3.582 8 8 8zm0-2c3.314 0 6-2.686 6-6s-2.686-6-6-6-6 2.686-6 6 2.686 6 6 6zm33.414-6l5.95-5.95L45.95.636 40 6.586 34.05.636 32.636 2.05 38.586 8l-5.95 5.95 1.414 1.414L40 9.414l5.95 5.95 1.414-1.414L41.414 8zM40 48c4.418 0 8-3.582 8-8s-3.582-8-8-8-8 3.582-8 8 3.582 8 8 8zm0-2c3.314 0 6-2.686 6-6s-2.686-6-6-6-6 2.686-6 6 2.686 6 6 6zM9.414 40l5.95-5.95-1.414-1.414L8 38.586l-5.95-5.95L.636 34.05 6.586 40l-5.95 5.95 1.414 1.414L8 41.414l5.95 5.95 1.414-1.414L9.414 40z' fill='%239C92AC' fill-opacity='0.4' fill-rule='evenodd'/%3E%3C/svg%3E");
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

.navbar-text {
  background-image: linear-gradient(white, white);
  background-size: 0 2px;
  background-repeat: no-repeat;
  background-position: left bottom;
  transition: background-size .25s ease;
}

.navbar-text:hover {
  background-size: 100% 2px;
}
</style>
