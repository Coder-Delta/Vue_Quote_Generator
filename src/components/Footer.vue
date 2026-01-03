<script setup>
import { ref } from "vue";

const currentYear = ref(new Date().getFullYear());
const href = ref("https://github.com/Coder-Delta");
</script>

<template>
  <footer>
    Created by
    <a v-bind:href="href" target="_blank">
        <!-- target="_blank" opens the link in a new tab -->
      <span>Coder-Delta</span>
    </a>
    @ {{ currentYear }}
  </footer>
</template>

<style scoped>
/* FOOTER CSS */
footer {
  position: fixed;
  margin: 0 auto;
  bottom: 0;
  width: 100%;
  text-align: center;
  color: #CCD6D9;
  padding-bottom: 20px;
}

span {
  font-family: cursive;
}
</style>
