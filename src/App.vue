<template>
  <div id="app">
    <div class="chessboard">
      <div class="row title">
        <div class="vertical">A</div><!--
        --><div class="vertical">B</div><!--
        --><div class="vertical">C</div><!--
        --><div class="vertical">D</div><!--
        --><div class="vertical">E</div><!--
        --><div class="vertical">F</div><!--
        --><div class="vertical">G</div><!--
        --><div class="vertical">H</div>
      </div>
      <br />
      <div class="row white">
        <div class="vertical"><span>1</span></div><!--
        --><div @click="select(1, 1)" v-bind:style="{ background: elementsColor[0][0]}"></div><!--
        --><div @click="select(1, 2)" v-bind:style="{ background: elementsColor[0][1]}"></div><!--
        --><div @click="select(1, 3)" v-bind:style="{ background: elementsColor[0][2]}"></div><!--
        --><div @click="select(1, 4)" v-bind:style="{ background: elementsColor[0][3]}"></div><!--
        --><div @click="select(1, 5)" v-bind:style="{ background: elementsColor[0][4]}"></div><!--
        --><div @click="select(1, 6)" v-bind:style="{ background: elementsColor[0][5]}"></div><!--
        --><div @click="select(1, 7)" v-bind:style="{ background: elementsColor[0][6]}"></div><!--
        --><div @click="select(1, 8)" v-bind:style="{ background: elementsColor[0][7]}"></div><!--
        --><div class="vertical"><span>1</span></div>
      </div>
      <br />
      <div class="row black">
        <div class="vertical"><span>2</span></div><!--
        --><div @click="select(2, 1)" v-bind:style="{ background: elementsColor[1][0]}"></div><!--
        --><div @click="select(2, 2)" v-bind:style="{ background: elementsColor[1][1]}"></div><!--
        --><div @click="select(2, 3)" v-bind:style="{ background: elementsColor[1][2]}"></div><!--
        --><div @click="select(2, 4)" v-bind:style="{ background: elementsColor[1][3]}"></div><!--
        --><div @click="select(2, 5)" v-bind:style="{ background: elementsColor[1][4]}"></div><!--
        --><div @click="select(2, 6)" v-bind:style="{ background: elementsColor[1][5]}"></div><!--
        --><div @click="select(2, 7)" v-bind:style="{ background: elementsColor[1][6]}"></div><!--
        --><div @click="select(2, 8)" v-bind:style="{ background: elementsColor[1][7]}"></div><!--
        --><div class="vertical"><span>2</span></div>
      </div>
      <br />
      <div class="row white">
        <div class="vertical"><span>3</span></div><!--
        --><div @click="select(3, 1)" v-bind:style="{ background: elementsColor[2][0]}"></div><!--
        --><div @click="select(3, 2)" v-bind:style="{ background: elementsColor[2][1]}"></div><!--
        --><div @click="select(3, 3)" v-bind:style="{ background: elementsColor[2][2]}"></div><!--
        --><div @click="select(3, 4)" v-bind:style="{ background: elementsColor[2][3]}"></div><!--
        --><div @click="select(3, 5)" v-bind:style="{ background: elementsColor[2][4]}"></div><!--
        --><div @click="select(3, 6)" v-bind:style="{ background: elementsColor[2][5]}"></div><!--
        --><div @click="select(3, 7)" v-bind:style="{ background: elementsColor[2][6]}"></div><!--
        --><div @click="select(3, 8)" v-bind:style="{ background: elementsColor[2][7]}"></div><!--
        --><div class="vertical"><span>3</span></div>
      </div>
      <br />
      <div class="row black">
        <div class="vertical"><span>4</span></div><!--
        --><div @click="select(4, 1)" v-bind:style="{ background: elementsColor[3][0]}"></div><!--
        --><div @click="select(4, 2)" v-bind:style="{ background: elementsColor[3][1]}"></div><!--
        --><div @click="select(4, 3)" v-bind:style="{ background: elementsColor[3][2]}"></div><!--
        --><div @click="select(4, 4)" v-bind:style="{ background: elementsColor[3][3]}"></div><!--
        --><div @click="select(4, 5)" v-bind:style="{ background: elementsColor[3][4]}"></div><!--
        --><div @click="select(4, 6)" v-bind:style="{ background: elementsColor[3][5]}"></div><!--
        --><div @click="select(4, 7)" v-bind:style="{ background: elementsColor[3][6]}"></div><!--
        --><div @click="select(4, 8)" v-bind:style="{ background: elementsColor[3][7]}"></div><!--
        --><div class="vertical"><span>4</span></div>
      </div>
      <br />
      <div class="row white">
        <div class="vertical"><span>5</span></div><!--
        --><div @click="select(5, 1)" v-bind:style="{ background: elementsColor[4][0]}"></div><!--
        --><div @click="select(5, 2)" v-bind:style="{ background: elementsColor[4][1]}"></div><!--
        --><div @click="select(5, 3)" v-bind:style="{ background: elementsColor[4][2]}"></div><!--
        --><div @click="select(5, 4)" v-bind:style="{ background: elementsColor[4][3]}"></div><!--
        --><div @click="select(5, 5)" v-bind:style="{ background: elementsColor[4][4]}"></div><!--
        --><div @click="select(5, 6)" v-bind:style="{ background: elementsColor[4][5]}"></div><!--
        --><div @click="select(5, 7)" v-bind:style="{ background: elementsColor[4][6]}"></div><!--
        --><div @click="select(5, 8)" v-bind:style="{ background: elementsColor[4][7]}"></div><!--
        --><div class="vertical"><span>5</span></div>
      </div>
      <br />
      <div class="row black">
        <div class="vertical"><span>6</span></div><!--
        --><div @click="select(6, 1)" v-bind:style="{ background: elementsColor[5][0]}"></div><!--
        --><div @click="select(6, 2)" v-bind:style="{ background: elementsColor[5][1]}"></div><!--
        --><div @click="select(6, 3)" v-bind:style="{ background: elementsColor[5][2]}"></div><!--
        --><div @click="select(6, 4)" v-bind:style="{ background: elementsColor[5][3]}"></div><!--
        --><div @click="select(6, 5)" v-bind:style="{ background: elementsColor[5][4]}"></div><!--
        --><div @click="select(6, 6)" v-bind:style="{ background: elementsColor[5][5]}"></div><!--
        --><div @click="select(6, 7)" v-bind:style="{ background: elementsColor[5][6]}"></div><!--
        --><div @click="select(6, 8)" v-bind:style="{ background: elementsColor[5][7]}"></div><!--
        --><div class="vertical"><span>6</span></div>
      </div>
      <br />
      <div class="row white">
        <div class="vertical"><span>7</span></div><!--
        --><div @click="select(7, 1)" v-bind:style="{ background: elementsColor[6][0]}"></div><!--
        --><div @click="select(7, 2)" v-bind:style="{ background: elementsColor[6][1]}"></div><!--
        --><div @click="select(7, 3)" v-bind:style="{ background: elementsColor[6][2]}"></div><!--
        --><div @click="select(7, 4)" v-bind:style="{ background: elementsColor[6][3]}"></div><!--
        --><div @click="select(7, 5)" v-bind:style="{ background: elementsColor[6][4]}"></div><!--
        --><div @click="select(7, 6)" v-bind:style="{ background: elementsColor[6][5]}"></div><!--
        --><div @click="select(7, 7)" v-bind:style="{ background: elementsColor[6][6]}"></div><!--
        --><div @click="select(7, 8)" v-bind:style="{ background: elementsColor[6][7]}"></div><!--
        --><div class="vertical"><span>7</span></div>
      </div>
      <br />
      <div class="row black">
        <div class="vertical"><span>8</span></div><!--
        --><div @click="select(8, 1)" v-bind:style="{ background: elementsColor[7][0]}"></div><!--
        --><div @click="select(8, 2)" v-bind:style="{ background: elementsColor[7][1]}"></div><!--
        --><div @click="select(8, 3)" v-bind:style="{ background: elementsColor[7][2]}"></div><!--
        --><div @click="select(8, 4)" v-bind:style="{ background: elementsColor[7][3]}"></div><!--
        --><div @click="select(8, 5)" v-bind:style="{ background: elementsColor[7][4]}"></div><!--
        --><div @click="select(8, 6)" v-bind:style="{ background: elementsColor[7][5]}"></div><!--
        --><div @click="select(8, 7)" v-bind:style="{ background: elementsColor[7][6]}"></div><!--
        --><div @click="select(8, 8)" v-bind:style="{ background: elementsColor[7][7]}"></div><!--
        --><div class="vertical"><span>8</span></div>
      </div>
      <br />
      <div class="row title">
        <div class="vertical">A</div><!--
        --><div class="vertical">B</div><!--
        --><div class="vertical">C</div><!--
        --><div class="vertical">D</div><!--
        --><div class="vertical">E</div><!--
        --><div class="vertical">F</div><!--
        --><div class="vertical">G</div><!--
        --><div class="vertical">H</div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',

  data() {
    return {
      // Предыдущая выбранная позиция
      elementPrev: [-1, -1],

      // Возможные позиции в виде (x, y)
      possibilites: [],

      // Цвета клеток шахматной доски
      elementsColor: [],

      /**
       * Текущий цвет для клетки:
       * 1, 2 - по-умолчанию (белая, либо чёрная)
       * 3 - выбранная клетка
       * 4 - возможная позиция
       */
      elementStatus: ['#FFFFFF', '#000000', '#0000FF', '#00FF00'],

      // Размер шахматной доски
      boardSize: 8,
    };
  },

  methods: {
    /**
     * Восстанавливаем цвета по-умолчанию
     * для предыдущей выбранной позиции и
     * возможных ходов.
     *
     * Окрашиваем выбранную позицию.
     * Окрашиваем все возможные позиции.
     */
    select(i, j) {
      console.log(`Checked: ${i} ${j}`);

      // Восстанавливаем цвет предыдущей выбранной клетки
      if ((this.elementPrev[0] !== -1)
        && (this.elementPrev[1] !== -1)
      ) {
        const x = this.elementPrev[0];
        const y = this.elementPrev[1];
        this.elementsColor[x][y] = this.elementStatus[(x + y) % 2];
      }

      // Сохраняем координаты выбранной клетки, и перекрашиваем её
      this.elementsColor[i - 1][j - 1] = this.elementStatus[2];
      this.elementPrev[0] = i - 1;
      this.elementPrev[1] = j - 1;

      /*
       * Восстанавливаем цвета клеток,
       * отмеченных как возможные ходы
       */
      this.possibilites.forEach((coord) => {
        const x = coord[0];
        const y = coord[1];
        this.elementsColor[x][y] = this.elementStatus[(x + y) % 2];
      });

      /**
       * Проверяем каждое возможное значение хода.
       * Сохраняем возможные.
       * Перекрашиваем соответствующие позиции.
       */
      this.possibilites = [];
      let coord = [i + 1, j - 2];
      if ((coord[0] < 8 && coord[1] < 8)
        && (coord[0] >= 0 && coord[1] >= 0)
      ) {
        this.possibilites.push(coord);
      }

      coord = [i + 1, j];
      if ((coord[0] < 8 && coord[1] < 8)
        && (coord[0] >= 0 && coord[1] >= 0)
      ) {
        this.possibilites.push(coord);
      }

      coord = [i, j + 1];
      if ((coord[0] < 8 && coord[1] < 8)
        && (coord[0] >= 0 && coord[1] >= 0)
      ) {
        this.possibilites.push(coord);
      }

      coord = [i - 2, j + 1];
      if ((coord[0] < 8 && coord[1] < 8)
        && (coord[0] >= 0 && coord[1] >= 0)
      ) {
        this.possibilites.push(coord);
      }

      coord = [i - 3, j];
      if ((coord[0] < 8 && coord[1] < 8)
        && (coord[0] >= 0 && coord[1] >= 0)
      ) {
        this.possibilites.push(coord);
      }

      coord = [i - 3, j - 2];
      if ((coord[0] < 8 && coord[1] < 8)
        && (coord[0] >= 0 && coord[1] >= 0)
      ) {
        this.possibilites.push(coord);
      }

      coord = [i - 2, j - 3];
      if ((coord[0] < 8 && coord[1] < 8)
        && (coord[0] >= 0 && coord[1] >= 0)
      ) {
        this.possibilites.push(coord);
      }

      coord = [i, j - 3];
      if ((coord[0] < 8 && coord[1] < 8)
        && (coord[0] >= 0 && coord[1] >= 0)
      ) {
        this.possibilites.push(coord);
      }

      this.possibilites.forEach((point) => {
        this.elementsColor[point[0]][point[1]] = this.elementStatus[3];
      });

      // Ререндер
      this.$forceUpdate();
    },

    // Сгенерировать цвета по-умолчаню для каждой клетки
    generate() {
      let row = [];

      for (let i = 0; i < this.boardSize; i += 1) {
        row = [];

        for (let j = 0; j < this.boardSize; j += 1) {
          row.push(this.elementStatus[(i + j) % 2]);
        }

        this.elementsColor.push(row);
      }
    },
  },

  created() {
    this.generate();
  },
};
</script>

<style>
#app {
  display: inline-block;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  margin: auto;
}

.horizontal {
  letter-spacing: 30px;
  padding-left: 30px;
}

.vertical {
  display: inline-block;
  text-align: center;
  line-height: 40px;
}

.row {
  margin: 0;
  display: inline-block;
}

.row div {
  vertical-align: top;
  display: inline-block;
  width: 40px;
  height: 40px;
  background-color: rgba(0, 0, 0, 0);
}

.title {
  margin-left: 40px;
}
/*
.white div:nth-child(even),
.black div:nth-child(odd)
{
  background-color: white;
}

.white div:nth-child(odd),
.black div:nth-child(even)
{
  background-color: black;
}
*/
.row div:nth-child(1),
.row div:nth-child(10) {
  background-color: rgba(0, 0, 0, 0);
}
</style>
