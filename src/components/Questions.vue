<template>
  <div class="wrapper">
    <div class="title">
      <h1>FAQ</h1>
    </div>
    <div class="questions">
      <div class="question-card" v-for="Ques in FAQ" :key="Ques.id">
        <div class="question" @click="openQuestion(Ques.id); addSelectedClass($event)">
          {{ Ques.question }}
          <img src="../assets/images/icon-arrow-down.svg" alt="">
        </div>
        <div class="answer" v-if="openedQuestionIndex == Ques.id">
          {{ Ques.answer }}
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import FAQ from '../assets/json/FAQ.json'

let openedQuestionIndex = ref(-1);

function openQuestion(id) {
  openedQuestionIndex.value = id;
}

function addSelectedClass(event) {
  const targetDiv = event.currentTarget
  const otherDivs = document.querySelectorAll('.question')

  console.log(targetDiv, otherDivs)

  otherDivs.forEach(div => {
    if (div != targetDiv) {
      div.classList.remove('selected')
    }
    else {
      div.classList.add('selected')
    }
  });
  // targetDiv.classList.add('selected')
}
</script>

<style scoped>
.wrapper {
  height: 100%;
  width: 50%;
  position: relative;
}

.title {
  margin-top: 60px;
  margin-bottom: 30px;
  margin-left: 20px;
}

.title h1 {
  margin: 0px;
}

.questions {
  margin-left: 20px;
}

.question-card {
  margin-top: 15px;
  margin-right: 100px;
  padding-bottom: 15px;
  border-bottom: 1px solid #e7e7e9;
}

.question {
  display: flex;
  justify-content: space-between;
  align-items: center;
  cursor: pointer;
}

.question:hover {
  color: #f47c57;
}

.question img {
  width: 10px;
  height: 7px;
  user-select: none;
  pointer-events: none;
}

.answer {
  margin-top: 10px;
}

.selected {
  font-weight: 700;
}

.selected:hover {
  color: #000000;
}
</style>