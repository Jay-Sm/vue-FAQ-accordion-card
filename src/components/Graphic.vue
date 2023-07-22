<template>
  <img class="box-graphic" src=".././assets/images/illustration-box-desktop.svg" alt="">
  <div class="wrapper">
    <img class="woman-graphic" src=".././assets/images/illustration-woman-online-desktop.svg" alt="">
    <img class="pattern-graphic" src=".././assets/images/bg-pattern-desktop.svg" alt="">
  </div>
</template>

<style scoped>
.wrapper {
  height: 100%;
  width: 50%;
  position: relative;
  user-select: none;
  pointer-events: none;
  overflow: hidden;
}

.box-graphic {
  width: 200px;
  position: absolute;
  top: 183px;
  left: -97px;
  z-index: 3;
  user-select: none;
  pointer-events: none;
}

.woman-graphic {
  width: 450px;
  position: absolute;
  top: 60px;
  left: -75px;
  z-index: 2;
}

.pattern-graphic {
  width: 800px;
  position: absolute;
  top: -232px;
  left: -424px;
  z-index: 1;
}
</style>