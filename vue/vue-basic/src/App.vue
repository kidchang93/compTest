<template>
  <div>
    <li>{{ sampleArray[0] }}</li>
    <li>{{ sampleArray[1] }}</li>
    <li>{{ sampleArray[2] }}</li>
    <li>{{ sampleArray[3] }}</li>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sampleArray: ["a", "b", "c", "d"],
    };
  },
};
</script>

<style lang="scss" scoped></style>
