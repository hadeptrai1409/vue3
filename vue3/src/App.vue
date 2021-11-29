<template>
  <div class="lh-fl">
    <ChillOne :tuoi="name"  />
    <ChillTwo :tuoi="name" @data:update="(e) => {name = }" />
    <!-- <Form /> -->
  </div>
</template>
<script>
import Form from "./components/Form.vue";
import ChillOne from "./components/ChillOne.vue";
import ChillTwo from "./components/ChillTwo.vue";
export default {
  name:'App',
  components:{
    ChillOne,
    ChillTwo,
    Form
  },
  data() {
    return {
      name: 30,
    };
  },
  methods: {
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
.lh-fl {
  display: flex;
  gap: 20px;
  justify-content: center;
}
</style>
