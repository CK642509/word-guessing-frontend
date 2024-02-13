<script setup lang="ts">
import { ref } from 'vue';
import wordbank from '@/utils/wordbank';

const correctCount = ref<number>(0);
const wrongCount = ref<number>(0);
const idx = ref<number>(0);

const detectClickSide = (event: MouseEvent) => {
  const rect = (event.target as HTMLElement).getBoundingClientRect();
  const middlePoint = rect.left + rect.width / 2;

  if (event.clientX < middlePoint) {
    console.log('Left side clicked');
    correctCount.value++;
  } else {
    console.log('Right side clicked');
    wrongCount.value++;
  }

  idx.value = Math.floor(Math.random() * wordbank.length);
};

</script>

<template>
  <v-card  @click="detectClickSide($event)">
    <!-- <v-card-title>Home</v-card-title> -->
    <v-card-text>
      <v-row>
        <v-col class="text-center">
          <a class="text-h1"> {{ wordbank[idx] }}</a>
        </v-col>
      </v-row>
      <v-row>
        <v-col class="text-center">
          Correct: {{ correctCount }}
        </v-col>
        <v-col class="text-center">
          Wrong: {{ wrongCount }}
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>
