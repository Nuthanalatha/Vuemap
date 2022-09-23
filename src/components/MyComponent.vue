<template>
  <h1>Hey This is My Component</h1>
  <h2>Name is:{{ name }} {{ greeting }}</h2>
  <!-- {{ value }} -->
  <p>userName is : {{ UserName }} rollNum:{{ rollNum }}</p>
</template>

<script>
export default {
  //props: ["greeting", "UserName", "rollNum", "value"],
  props: {
    greeting: {
      type: String,
      required: true,
    },
    UserName: {
      type: String,
    },
    rollNum: {
      type: Number,
      default: 90,
    },
  },

  data() {
    return {
      name: "Ajay",
    };
  },
};
</script>

<style></style>
