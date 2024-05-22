<template>
  <div>{{ count }}</div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  beforeCreate() {
    console.log("LifeCycle is beforeCreate: ", this.count);
  },
  created() {
    console.log("LifeCycle is Created: ", this.count);
  },
};
</script>

<style lang="scss" scoped></style>
