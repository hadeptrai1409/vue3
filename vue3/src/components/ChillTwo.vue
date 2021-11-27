<template>
  <div class="clear">
    <h1>Chill Two</h1>
    <div class="component">
      <h3>User Details</h3>
      <p>Tuổi tôi là - {{ tuoi }}</p>
      <button @click="changeAge">Click</button>
    </div>
  </div>
</template>
<script>
export default {
  name:'child2',
  emits:['data:update'],
  props: ["tuoi"],
  methods: {
    changeAge() {
      console.log("click");
      this.$emit("data:update", 24);
    },
  },
};
</script>
