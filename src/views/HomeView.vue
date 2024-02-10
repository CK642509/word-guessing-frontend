<script setup lang="ts">
import { ref } from 'vue';
const correctCount = ref(0);
const wrongCount = ref(0);

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
};

</script>

<template>
  <v-card  @click="detectClickSide($event)">
    <v-card-title>Home</v-card-title>
    <v-card-text>
      <v-row>
        <v-col>
          Apple
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          Correct: {{ correctCount }}
        </v-col>
        <v-col>
          Wrong: {{ wrongCount }}
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>
