<template>
  <div v-bind:class="classNname">
    <input type="text" v-model="character" />
    <div v-if="character == 'A'">A</div>
    <div v-else-if="character == 'B'">B</div>
    <div v-else>C</div>

    <div v-for="c in country" :key="c.code">
      {{ c.name }}
    </div>

    <div v-for="(value, key) in personInfo" :key="key">
      {{ key }} : {{ value }}
    </div>
  </div>
</template>
        
<script>
import Third from "./Third.vue";
export default {
  name: "First",
  data() {
    return {
      msgf: "Hi mohamed anwar first",
      number: 123,
      skills: ["html", "css", "js"],
      person: {
        name: "mohamed",
        age: 25,
      },
      available: true,
      classNname: "first",
      link: "https://www.google.com",
      selected: " ",
      character: "B",
      country: [
        { name: "Egypt", code: "EG" },
        { name: "USA", code: "US" },
        { name: "UK", code: "UK" },
        { name: "France", code: "FR" },
        { name: "Germany", code: "DE" },
        { name: "Italy", code: "IT" },
      ],

      personInfo: {
        name: "mohamed",
        age: 25,
        skills: ["html", "css", "js"],
      },
    };
  },
  methods: {},
  beforeCreate() {
    console.log("beforeCreate");
  },
  created() {
    console.log("created");
  },
  beforeMount() {
    console.log("beforeMount");
  },
  mounted() {
    console.log("mounted");
  },
  beforeUpdate() {
    console.log("beforeUpdate");
  },
  updated() {
    console.log("updated");
  },
  beforeDestroy() {
    console.log("beforeDestroy");
  },
  destroyed() {
    console.log("destroyed");
  },
};
</script>
        
<style scoped>
.first {
  background-color: #f00;
}
.c1 {
  color: green;
}
</style>


