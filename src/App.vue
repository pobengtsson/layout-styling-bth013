<template>
  <div class="app">
    <ResponsiveCard
      v-for="card in cardList"
      :key="card.id"
      :description="card.description"
      :title="card.title"
      :imagepath="card.imagepath"
      />
  </div>
</template>

<script setup>
import ResponsiveCard from './components/ResponsiveCard.vue'

const cardList = [
  {
    id: 928347,
    title: "Yosemite National Park, USA",
    description: "Explore the vast wilderness of Yosemite with its towering cliffs, ancient giant sequoias, and stunning waterfalls. A hiker's paradise, offering trails for all levels.",
    imagepath: "images/yosemite.jpeg"
  },
  {
    id: 476591,
    title: "Torres del Paine, Chile",
    description: "Located in the Southern Patagonian Ice Field, the jagged mountains and blue glaciers make Torres del Paine a spectacular hiking destination.",
    imagepath: "images/torresdelpaine.jpeg"
  },
  {
    id: 302985,
    title: "Mount Kilimanjaro, Tanzania",
    description: "Africa's highest peak presents trekkers with a variety of ecosystems, from lush rainforests to alpine meadows and arctic summits.",
    imagepath: "images/kilimanjaro.jpeg"
  },
  {
    id: 884201,
    title: "Banff National Park, Canada",
    description: "Discover the rugged beauty of the Canadian Rockies with breathtaking scenery, crystalline lakes, and diverse wildlife.",
    imagepath: "images/banff.jpeg"
  },
  {
    id: 665309,
    title: "The Alps, Europe",
    description: "Traverse the iconic Alpine landscapes of Europe, featuring snowy peaks, verdant valleys, and picturesque villages.",
    imagepath: "images/alps.jpeg"
  },
  {
    id: 557982,
    title: "Annapurna Circuit, Nepal",
    description: "This trek offers a unique blend of Nepali culture and dramatic Himalayan landscapes, including high passes and serene Tibetan villages.",
    imagepath: "images/annapurna.jpeg"
  },
  {
    id: 139875,
    title: "Fiordland National Park, New Zealand",
    description: "Known for its fjords, towering peaks, and deep lakes, Fiordland is a must-visit for those who seek wilderness and solitude.",
    imagepath: "images/fiordland.jpeg"
  }
]
</script>

<style scoped>
.app {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  flex-wrap: wrap;
  gap: 20px;
  background-color: #f5f5f5;
}
</style>
