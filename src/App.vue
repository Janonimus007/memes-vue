<template>
  <!-- <h1>{{ $store.state.titleApp }}</h1> -->
  <!-- <h1 class="container">{{ titleApp }}</h1> -->
  <div class="container">
    <ListMemes />
  </div>
</template>

<script>
import { useStore } from "vuex";
import ListMemes from "./components/ListMemes.vue";

export default {
  name: "App",
  components: {
    ListMemes,
  },
  setup() {
    const store = useStore();
    const title = store.state.titleApp;
    console.log("STATE", store.state.titleApp);
    return {
      ...store.state,
    };
  },
};
</script>

<style>
</style>
