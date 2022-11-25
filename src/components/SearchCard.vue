<template>
  <Card>
    <input type="text" placeholder="enter name" v-model="searchString"/>
    <ul id="example-1" class="list">
      <li v-for="item in items" :key="item">
        {{ item.includes(searchString) ? item : "" }}
      </li>
    </ul>
  </Card>
</template>

<script>
import Card from "./Card.vue"

export default {
  components: {
    Card
  },
  props: {
    items: {
      type: Array
    }
  },
  data() {
    return {
      searchString: ""
    }
  },
}
</script>

<style scoped>
.list {
  margin: 10px 0;
  list-style-type: none;
  padding-left: 0;
}
</style>