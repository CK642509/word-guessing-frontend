<script setup lang="ts">

const detectClickSide = (event: MouseEvent) => {
  const rect = (event.target as HTMLElement).getBoundingClientRect();
  const middlePoint = rect.left + rect.width / 2;

  if (event.clientX < middlePoint) {
    console.log('Left side clicked');
  } else {
    console.log('Right side clicked');
  }
};

</script>

<template>
  <v-card  @click="detectClickSide($event)">
    <v-card-title>Home</v-card-title>
    <v-card-text>
      <p>Welcome to the home page</p>
    </v-card-text>
  </v-card>
</template>
