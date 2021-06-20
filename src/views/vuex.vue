<template>
  <div>
    以下是从store中取出来的数据
    <br />
    <b>count: {{ count }}</b>
    <br />
    <b>double: {{ double }}</b>
    <br />
    <button @click="handleClickBtn">increment</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, computed } from "vue";
import { useStore } from "vuex";

export default defineComponent({
  name: "Vuex",
  setup() {
    const store = useStore();
    const handleClickBtn = () => {
      store.commit("increment");
    };
    return {
      handleClickBtn,
      count: computed(() => store.state.count),
      double: computed(() => store.getters.double),
    };
  },
});
</script>

<style scoped></style>
