<template>
  <router-view></router-view>
</template>

<script setup>
</script>

<style>
:root{
  font-family: 'Kumbh Sans', sans-serif;
}

html{
  height: 100%;
}

body {
  height: 100vh;
  margin: 0px;
  
  background: rgb(175, 103, 233);
  background: linear-gradient(180deg, rgba(175, 103, 233, 1) 0%, rgba(101, 101, 231, 1) 100%);
}

#app {
  height: 100%;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>