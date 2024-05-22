<template>
  <div>
    <!-- v-for 디렉티브를 사용 -->
    <li v-for="item in sampleArray">{{ item }}</li>
    <!-- 기존 HTML 코드 작성 방식 -->
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
