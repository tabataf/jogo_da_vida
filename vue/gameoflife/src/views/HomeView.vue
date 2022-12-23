<template>
  <div class="home">
    <HelloWorld msg="Game of Life - by Tábata de Faria" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld,
  },
};
</script>
