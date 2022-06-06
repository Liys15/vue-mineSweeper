<script setup lang="ts">
import { ref } from 'vue'
import { gameBoardCols, gameBoardRows } from '../func/gameConstants'



</script>

<template>
  <div class="gameBoard">
    <div class="board-row" v-for="row, idx1 in gameBoardRows">
      <div class="board" v-for="col, idx2 in gameBoardCols">{{ idx1 }}, {{ idx2 }}</div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.gameBoard {
  height: 80vh;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
}

.board-row {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

.board {
  background-color: #eee;
  width: 100px;
  height: 100px;
  margin: 2px;
  line-height: 100px;

  &:hover {
    background-color: #999;
  }
}
</style>
