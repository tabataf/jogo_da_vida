<template>
  <div>
    <div class="tabuleiro">
      <div class="tabuleiro_linha">
        <div id="l1c1" class="quadrado"></div>
        <div id="l1c2" class="quadrado"></div>
        <div id="l1c3" class="quadrado"></div>
        <div id="l1c4" class="quadrado"></div>
        <div id="l1c5" class="quadrado"></div>
      </div>
      <div class="tabuleiro_linha">
        <div id="l2c1" class="quadrado"></div>
        <div id="l2c2" class="quadrado"></div>
        <div id="l2c3" class="quadrado"></div>
        <div id="l2c4" class="quadrado"></div>
        <div id="l2c5" class="quadrado"></div>
      </div>
      <div class="tabuleiro_linha">
        <div id="l3c1" class="quadrado"></div>
        <div id="l3c2" class="quadrado"></div>
        <div id="l3c3" class="quadrado"></div>
        <div id="l3c4" class="quadrado"></div>
        <div id="l3c5" class="quadrado"></div>
      </div>
      <div class="tabuleiro_linha">
        <div id="l4c1" class="quadrado"></div>
        <div id="l4c2" class="quadrado"></div>
        <div id="l4c3" class="quadrado"></div>
        <div id="l4c4" class="quadrado"></div>
        <div id="l4c5" class="quadrado"></div>
      </div>
      <div class="tabuleiro_linha">
        <div id="l5c1" class="quadrado"></div>
        <div id="l5c2" class="quadrado"></div>
        <div id="l5c3" class="quadrado"></div>
        <div id="l5c4" class="quadrado"></div>
        <div id="l5c5" class="quadrado"></div>
      </div>
      <div class="tabuleiro_linha">
        <div id="l6c1" class="quadrado"></div>
        <div id="l6c2" class="quadrado"></div>
        <div id="l6c3" class="quadrado"></div>
        <div id="l6c4" class="quadrado"></div>
        <div id="l6c5" class="quadrado"></div>
      </div>
    </div>
    <a class="link" href="https://github.com/tabataf">By: Tábata de Faria</a>
  </div>
</template>

<script>
// import { METHODS } from 'http';
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  // methods: {
  //   q= false
  // }
};
</script>
<style scoped>
.vivo {
  background-color: aquamarine;
}
.quadrado {
  border: pink 0.5px solid;
  border-collapse: separate;
  width: 30px;
  height: 30px;
  display: inline-block;
}
.link {
  color: rgb(132, 127, 131);
}
.tabuleiro_linha {
  margin: 0;
  display: flex;
}

.tabuleiro {
}

.vivo {
  background-color: rgb(164, 150, 206);
}
</style>
