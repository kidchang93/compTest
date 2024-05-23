<template>
  <div>
    <ChildComponent
      :send-props1="title"
      :send-props2="createdAt"
      :send-props3="obj"
    />
  </div>
</template>

<script setup lang="ts">
import { reactive, ref } from "vue";
import ChildComponent from "./components/ChildComponent.vue";

interface obj {
  id: Number;
  name: String;
}

const title = ref<String>("부모 컴포넌트에서 선언된 내용입니다.");
const createdAt = ref<Number>(2024);
const obj = reactive({
  id: 2024,
  name: "john",
});
</script>

<style scoped></style>
