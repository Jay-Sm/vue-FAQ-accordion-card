<template>
  <div class="main">
    <Graphic />
    <Questions />
  </div>
</template>

<script setup>
import Questions from '../components/Questions.vue'
import Graphic from '../components/Graphic.vue'

</script>

<style>
.main {
  width: 900px;
  height: 500px;
  background-color: #ffffff;
  box-sizing: border-box;
  border-radius: 23px;

  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  position: fixed;
}

@media (max-width: 930px) {
  .main {
    width: 840px;
  }

}
</style>