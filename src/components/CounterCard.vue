<template>
  <Card>
    <h2>{{value}}</h2>
    <button class="button" @click="incrementCounter">increment</button>
    <button class="button" @click="decrementCounter">decrement</button>
  </Card>
</template>

<script>
import Card from "./Card.vue"

export default {
  components: {
    Card
  },
  props: {
    defaultValue: Number
  },
  data() {
    return {
      value: 0
    };
  },
  methods: {
    incrementCounter() {
      this.value++;
    },
    decrementCounter() {
      this.value--;
    }
  },
  mounted() {
    this.value = this.$props.defaultValue
  },
};
</script>

<style scoped>
.button {
  margin-right: 5px;
}
</style>