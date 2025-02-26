<template>
  <div class="card">
    <img :src="imagepath">
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>
    <button>Read More</button>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const { title, description, imagepath } = defineProps({
  title: {},
  description: {},
  imagepath: {},
})
</script>

<style scoped lang="scss">
@use '../styles/variables' as *;

h2, p {
  overflow: hidden;
  max-width: 95%;
}

h2 {
  text-overflow: ellipsis;
  white-space: nowrap;
  margin-bottom: .2em;
  margin-top: .2em;
}

p {
  margin-top: .5em;
  padding-top: 0em;
  height: 3.5em;
}

.card {
  background-color: $background-color;
  color: $text-color;
  border: 1px solid $primary-color;
  border-radius: 8px;
  padding: 20px;
  margin: 20px;
  width: 30vw;
  // height: 80vh;
  flex: 0 1 auto;
  display: flex;
  flex-direction: column;
  text-align: left;

  img {
    max-width: 100%;
    border-radius: 4px;
  }

  @media (max-width: 600px) {
    width: 100%;
  }
}
</style>
