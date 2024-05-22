<template>
  <div>
    <!-- v-for 디렉티브를 사용 -->
    <li
      v-for="(item, index) in sampleArray"
      :key="item"
      @click="openDialog(index)"
    >
      {{ item }} / {{ index }}
    </li>
    <li v-for="(user, index) in otherArray" :key="user.name">
      {{ user.id }} / {{ user.name }} / {{ index }}
    </li>
    <!-- 기존 HTML 코드 작성 방식 -->
    <!-- <li>{{ sampleArray[0] }}</li>
    <li>{{ sampleArray[1] }}</li>
    <li>{{ sampleArray[2] }}</li>
    <li>{{ sampleArray[3] }}</li> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      sampleArray: ["a", "b", "c", "d"],
      otherArray: [
        { id: 0, name: "john" },
        { id: 1, name: "kim" },
        { id: 2, name: "lee" },
        { id: 3, name: "park" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
