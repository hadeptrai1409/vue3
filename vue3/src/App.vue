<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import HelloWorld from "./components/HelloWorld.vue";
import Form from "./components/Form.vue";
import ChillOne from "./components/ChillOne.vue";
import ChillTwo from "./components/ChillTwo.vue";
</script>

<template>
  <Form />
  <div class="lh-fl">
    <chill-one :tuoi="name" @data:update="() => { console.log('ahihi') }" />
    <chill-two :tuoi="name" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: 30,
    };
  },
  methods: {},
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
