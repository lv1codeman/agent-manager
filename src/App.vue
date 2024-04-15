<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import { DownCircleOutlined } from "@ant-design/icons-vue";
import { ref, toRef } from "vue";

const items = ref([
  "Button 1",
  "Button 2",
  "Button 3",
  "Button 4",
  "Button 5",
  "Button 6",
  "Button 7",
]);
const size = "small";
</script>

<template>
  <a-button v-for="item in items" :key="item">{{ item }}</a-button>

  <div>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
  </div>
  <RouterView />
</template>

<style scoped></style>
