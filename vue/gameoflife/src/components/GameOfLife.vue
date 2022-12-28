<template>
  <div class="centralizar">
    <table>
      <tr v-for="(line, i) in grid" :key="i" class="quadrado">
        <td
          v-for="(cell, j) in line"
          :key="j"
          :class="{ vivo: cell == 1 }"
          class="quadrado"
        ></td>
      </tr>
    </table>
    <a class="link" href="https://github.com/tabataf">By: Tábata de Faria</a>
  </div>
</template>

<script>
function _count_vizinhos_vivos(i, j, grid) {
  const [M, N] = [grid.length, grid[0].length];
  const delta_coord = [
    [-1, -1],
    [-1, 0],
    [-1, 1],
    [0, -1],
    [0, 1],
    [1, -1],
    [1, 0],
    [1, 1],
  ];
  let coord_vizinhos = [];
  for (let k = 0; k < delta_coord.length; k++) {
    coord_vizinhos.push([i + delta_coord[k][0], j + delta_coord[k][1]]);
  }
  let coord_vizinhos_vivos = coord_vizinhos.filter(
    (e) =>
      e[0] >= 0 && e[0] < M && e[1] >= 0 && e[1] < N && grid[e[0]][e[1]] == 1
  );
  return coord_vizinhos_vivos.length;
}

function _nextState(grid) {
  const [M, N] = [grid.length, grid[0].length];
  let newGrid = new Array(M);
  for (let i = 0; i < M; i++) {
    newGrid[i] = new Array(N).fill(0);
  }
  for (let i = 0; i < M; i++) {
    for (let j = 0; j < N; j++) {
      let vizinhosvivos = _count_vizinhos_vivos(i, j, grid);
      if (grid[i][j] == 1) {
        if (vizinhosvivos == 2 || vizinhosvivos == 3) {
          newGrid[i][j] = 1;
        } else {
          newGrid[i][j] = 0;
        }
      } else {
        if (vizinhosvivos == 3) {
          newGrid[i][j] = 1;
        } else {
          newGrid[i][j] = 0;
        }
      }
    }
  }
  return newGrid;
}
export default {
  name: "GameOfLife",
  data() {
    return {
      grid: [
        [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
        [0, 0, 0, 1, 1, 0, 0, 0, 0, 0],
        [0, 0, 1, 0, 1, 0, 0, 0, 0, 0],
        [0, 0, 0, 0, 1, 0, 0, 0, 0, 0],
        [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
        [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
        [0, 0, 0, 0, 0, 0, 0, 0, 1, 0],
        [1, 0, 1, 0, 0, 0, 1, 1, 1, 0],
        [1, 1, 0, 0, 0, 0, 1, 1, 0, 0],
        [1, 0, 0, 0, 0, 0, 1, 0, 1, 1],
      ],
    };
  },
  methods: {
    nextstep() {
      this.grid = _nextState(this.grid);
    },
  },
  mounted() {
    Window.HelloWorld = this;
    setInterval(() => {
      this.nextstep();
    }, 1000);
  },
};
</script>
<style scoped>
.quadrado {
  border: pink 0.2px solid;
  border-collapse: separate;
  width: 30px;
  height: 30px;
  display: revert;
}
.link {
  margin-top: 2rem;
  color: rgb(132, 127, 131);
}

.link :hover {
  color: rgb(245, 92, 117);
}

.tabuleiro_linha {
  margin: 0;
  display: flex;
}
.centralizar {
  display: flex;
  align-items: center;
  flex-direction: column;
}
table {
  border-spacing: 0;
}
.vivo {
  background-color: rgb(245, 92, 117);
}
</style>
