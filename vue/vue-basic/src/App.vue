<template>
  <div>
    <button v-on:click="count++">인라인 핸들러</button>
    <h1>{{ count }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
};
</script>

<style lang="scss" scoped></style>
