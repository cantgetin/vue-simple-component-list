<template>
  <div class="card" :style="`background: ${color}`">
    <h1>{{ title }}</h1>
    <slot></slot>
    <h4>{{ color }}</h4>
  </div>
</template>

<script>
export default {
  props: {
    color: String,
    title: String,
    children: HTMLElement
  }
};
</script>

<style scoped>
.card {
  height: 400px;
  width: 20vw;
  min-width: 300px;
  padding: 20px;
  position: relative;
}

.card h1 {
  margin-bottom: 20px;
}

.card h4 {
  position: absolute;
  bottom: 20px;
  right: 20px;
}
</style>