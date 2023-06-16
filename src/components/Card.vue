<script setup>
import { defineProps } from 'vue';
//* returns Proxy
const {quiz} = defineProps(['quiz']);

</script>
<template>
    <div class="card">
        <img :src="quiz.img" alt="">
        <div class="card-text">
          <h2>{{quiz.name}}</h2>
          <p>{{ quiz.questions.length }} Questions</p>
        </div>
      </div>
</template>


<style scoped lang="scss">
.card {
  width: 310px;
  overflow: hidden;
  border-radius: 2%;
  box-shadow: 1px 1px 10px rgba(0, 0, 0, .1);
  cursor: pointer;
  margin: 0px 20px 35px 0; 

  img {
    width: 100%;
    height: 190px;
    margin: 0px;
  }

  &-text {
    padding: 0 5px;

    h2 {
      font-weight: bold;
    }
  }
}


</style>