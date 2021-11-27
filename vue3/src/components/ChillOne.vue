<template>
  <div class="clear">
    <h1>Chill One</h1>
    <p>Tuổi tôi là - {{ tuoi }}</p>
    <input type="text" v-model="proshow" />
    <ul>
      <li v-for="pro in one" :key="pro">
        <p>{{ pro }}</p>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      products: ["Iphone", "Ipad", "Nokia", "Samsung", "Vetur"],
      proshow: "",
    };
  },
  computed: {
    one() {
      return this.products.filter((e) => {
        return e.match(this.proshow);
      });
    },
  },
  methods: {
    clickFn() {
      this.tuoi = 10;
      console.log(this.tuoi);
      this.$emit("clickemit", this.tuoi);
    },
  },
  props: ["tuoi"],
};
</script>
