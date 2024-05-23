<template>
  <div>
    <ChildComponent
      v-bind:sendProps1="title"
      v-bind:sendProps2="createAt"
      v-bind:sendProps3="obj"
    ></ChildComponent>
  </div>
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: { ChildComponent },
  data() {
    return {
      title: "부모 컴포넌트에서 선언된 내용입니다.",
      createAt: 2024,
      obj: {
        id: 2024,
        name: "john",
      },
    };
  },
};
</script>

<style lang="scss" scoped></style>
