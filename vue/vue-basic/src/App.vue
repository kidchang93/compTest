<template>
  <div>
    <h1>{{ text }}</h1>
    <h1>changeText 함수 호출 값: {{ changeText() }}</h1>
    <h1>changeText 함수 호출 값: {{ changeText() }}</h1>
    <h1>changeText 함수 호출 값: {{ changeText() }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: "Computed Test 데이터 문구입니다.",
    };
  },
  methods: {
    changeText() {
      console.log("함수 호출");
      console.log(this.text);
      return this.text.split("").reverse().join("");
    },
  },
  // methods 부분에 선언된 동일한 logic일때
  // 캐싱 기능이 없는 methods 는 호출될때마다 console 값이 출력이 되었습니다.
  // 반면에, computed는 캐싱기능이 있기 떄문에 methods 와 어떤 차이점이 있는지
  // 주의깊게 살펴봐야한다.
  computed: {},
};
</script>

<style lang="scss" scoped></style>
