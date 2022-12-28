<template>
  <div class="home">
    <GameOfLife msg="Game of Life - by Tábata de Faria" />
  </div>
</template>

<script>
// @ is an alias to /src
import GameOfLife from "@/components/GameOfLife.vue";

export default {
  name: "GameLife",
  components: {
    GameOfLife,
  },
};
</script>
