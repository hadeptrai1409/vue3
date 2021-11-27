<template>
  <div class="clear">Thạch Hoàng Hà</div>
  {{ message }}
  <button @click="clickMes()">Click</button>
</template>
<script>
export default {
  data() {
    return {
      message: "I Am Thạch hOÀNG Hà",
    };
  },
  watch: {
    message() {
      alert("Hà đây");
    },
  },
  methods: {
    clickMes() {
      return (this.message = "Dữ Liệu đã được thay đổi");
    },
  },
};
</script>
