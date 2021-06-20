<template>
  以下是从store中取出来的数据
  <br />
  <b>count: {{ count }}</b>
  <br />
  <b>double: {{ double }}</b>
  <br />
  <button @click="handleClickBtn">increment</button>
</template>

<script lang="ts">
import { ref, defineComponent, computed } from "vue";
import HelloWorld from "@/components/HelloWorld.vue";
import { useStore } from "vuex";
export default defineComponent({
  name: "Vuex",
  setup: function () {
    const store = useStore();
    const handleClickBtn = () => {
      store.commit("increment");
    };
    return {
      handleClickBtn,
      count: computed(() => store.state.count),
      double: computed(() => store.getters.double)
    };
  }
});
</script>

<style scoped></style>
