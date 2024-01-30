<script setup>
import Accordion from "../components/Accordion.vue"
import {firesQuestion} from "../data"

</script>

<template>
  <section class="container max-w-[1150px] flex items-center gap-[50px] justify-between h-screen">
    <div class="w-full md:w-1/2 h-fit">
     <h1 class="text-[#283F75] text-[34px] mb-[30px]">
      На что рассчитывать при <br>
      взыскании неустойки по ДДУ?
     </h1>
     <p class="text-[#5B5B5B]">
      Когда застройщик нарушает сроки сдачи по ДДУ, вы как дольщик имеете право требовать неустойку за просрочку, 
      а также компенсацию убытков, вызванных этой просрочкой.
      <br>
      <br>
      Само собой, застройщику невыгодно добровольно выплачивать вам компенсацию. 
      Когда дело доходит до суда, суд урезает сумму неустойки на основании ст. 333 ГК РФ. Это урезание практически неизбежно.
     <br>
     <br>
      Основная наша задача состоит в том, чтобы взыскать неустойку по ДДУ в максимальном размере, т.е. избежать сильного ее урезания. 
      Вот что вы можете требовать от застройщика.
     </p>
    </div>
    <div class="w-full md:w-1/2">
      <Accordion
        v-for="(question, index) in firesQuestion"
        :key="index"
        :aria-title="question['aria-title']"
        :title="question.title"
        :description="question.description"
      ></Accordion>
    </div>
  </section>
</template>
