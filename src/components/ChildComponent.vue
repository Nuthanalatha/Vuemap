<template>
  <h1>Hi i am child component</h1>
  <button @click="handleClick">Send data to parent</button>
</template>

<script>
export default {
  emits: ["getDataFromChild"],
  data() {
    return {
      toyInfo: "red toy car",
    };
  },
  methods: {
    handleClick() {
      //   console.log("handleClick executed");
      this.$emit("getDataFromChild", this.toyInfo);
    },
  },
};
</script>

<style></style>
