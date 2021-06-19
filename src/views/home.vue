<template>
  <h1>this is home page</h1>
  <br />
  <img alt="Vue logo" src="../assets/logo.png" />
  <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
</template>

<script lang="ts">
import { ref, defineComponent } from "vue";
import HelloWorld from "@/components/HelloWorld.vue";
export default defineComponent({
  name: "Home",
  components: {
    HelloWorld,
  },
});
</script>

<style scoped></style>
