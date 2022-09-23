<template>
  <h1>Hello World</h1>

  <!-- rendering MyComponent -->
  <!-- /<my-component greeting="Good Morning" :UserName="UserName" :rollNum="130" /> -->
  <!-- :value="value" -->
  <!-- we give v-bind(:) to use dynamic properties UserName -->

  <!-- sending function to child component use v-on or @ -->
  <child-component @getDataFromChild="getDataFromChild" />

  <h3>Toy Data from child : {{ kidsToyData }}</h3>
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";
// import MyComponent from "./components/MyComponent.vue";
export default {
  name: "App",
  components: {
    // MyComponent,
    ChildComponent,
  },
  //data
  data() {
    return {
      UserName: "Raju Rastogi",
      value: true,
      kidsToyData: "",
    };
  },
  methods: {
    //chocholate function
    //1.in parent component a function and pass it to child component
    //2.call that function in child component and pass the data inside that function

    getDataFromChild(childData) {
      console.log("chocholate function executed", childData);
      this.kidsToyData = childData;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
