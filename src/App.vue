<script setup lang="ts">
import Card from "./components/Card.vue";

const tilePrompts = [
  {
    label: "Build a Login Page",
    description:
      "Create a clean login UI with email and password inputs and a submit button.",
  },
  {
    label: "Style a Pricing Table",
    description:
      "Design a 3-column pricing layout with highlighted features and a recommended plan.",
  },
  {
    label: "Animate a Button",
    description:
      "Add hover and click animations to a button for a more interactive user experience.",
  },
  {
    label: "Design a Blog Card",
    description:
      "Layout an article preview card with image, title, summary, and a “Read More” link.",
  },
  {
    label: "Build a Navigation Bar",
    description:
      "Create a responsive navbar with a logo, links, and a mobile menu toggle button.",
  },
];
</script>

<template>
  <div class="page-wrapper">
    <div class="card-grid">
      <Card v-for="tile in tilePrompts" :tile="tile" />
    </div>
  </div>
</template>

<style>
.page-wrapper {
  padding: 0 32px;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.card-grid {
  /* padding-top: 10px; */
  display: flex;
  overflow-x: scroll;
  gap: 8px;
}

/* .card-grid:has(.card:hover) .card:not(:hover),
.card-grid:has(.card:focus) .card:not(:focus) {
  opacity: 0.5;
} */
</style>
