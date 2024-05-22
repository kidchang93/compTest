<template>
  <div>{{ rawHtml }}</div>
  <div>{{ rawHtml2 }}</div>
  <!-- 아래가 정상 작동 -->
  <h1 v-html="rawHtml2"></h1>
</template>

<script>
export default {
  data() {
    return {
      rawHtml: "이것은 텍스트입니다.",
      rawHtml2: '<span style="color:red">이것은 빨간색 이어야 합니다.</span>',
    };
  },
};
</script>

<style lang="scss" scoped></style>
