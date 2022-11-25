<template>
  <Card>
    <h2>{{ value }}</h2>
    <input class="input-range" type="range" v-model="value" :min="min" :max="max"/>
    <div class="min-max">
      <h4>{{min}}</h4>
      <h4>{{max}}</h4>
    </div>
  </Card>
</template>

<script>
import Card from "./Card.vue"

export default {
  props: {
    min: Number,
    max: Number,
    defaultValue: Number
  },
  components: {
    Card
  },
  data() {
    return {
      title: "Range",
      value: 0
    };
  },
  mounted() {
    this.value = this.$props.defaultValue
  },
}
</script>

<style scoped>
.input-range {
  width: 100%;
}

.min-max {
  display: flex;
  justify-content: space-between;
}
</style>