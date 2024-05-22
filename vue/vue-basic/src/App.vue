<template>
  <div>{{ rawHtml }}</div>
  <div>{{ rawHtml2 }}</div>
  <!-- 아래가 정상 작동 -->
  <h1 v-html="rawHtml2"></h1>
  <!-- 아래 두개는 똑같다. 단지 좀 짧은 버전 -->
  <h2 v-bind:class="{ active: isActive }">클래스 바인딩 테스트 입니다.</h2>
  <h2 :class="{ active: isActive }">미쳤다</h2>
  <button @click="change">버튼</button>
  <!-- isActive 가 True 여야만 활성화가 된다. -->
  <!-- 스타일 바인딩 테스트 (인라인)-->
  <h3 style="color: red; font-size: 24px">스타일 바인딩 테스트입니다.</h3>
  <!-- 하드코딩 스타일 -->
  <h3 :style="{ color: fontColor, fontSize: fontSize + 'px' }">
    스타일 바인딩 테스트입니다.
  </h3>
</template>

<script>
export default {
  data() {
    return {
      rawHtml: "이것은 텍스트입니다.",
      rawHtml2: '<span style="color:red">이것은 빨간색 이어야 합니다.</span>',
      isActive: false,
      fontColor: "#887766",
      fontSize: 48,
    };
  },
  methods: {
    change() {
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style scoped>
h2.active {
  color: green;
}
</style>
