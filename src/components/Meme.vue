<template>
  <div class="col-3 meme">
    <p>{{ meme.name }}</p>
    <img :src="meme.url" :alt="meme.name" :class="fluid" />
  </div>
</template>

<script>
export default {
  props: {
    meme: Object,
  },
};
</script>

<style scoped>
.meme {
  height: 300;
  display: flex;
  flex-direction: column;
  align-items: center;
  border: 1px solid greey;
}
.meme img {
  max-height: 200px;
  max-width: 250px;
}
</style>