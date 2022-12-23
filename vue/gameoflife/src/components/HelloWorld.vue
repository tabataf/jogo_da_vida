<template>
  <div>
    <h1>{{ msg }}</h1>
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
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>
<style scoped>
.quadrado {
  border: pink 0.5px solid;
  border-collapse: separate;
  width: 20px;
  height: 20px;
  display: inline-block;
}

.tabuleiro_linha {
  margin: 0;
  display: flex;
}
</style>
