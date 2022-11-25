<template>
  <Card>
    <h3>
      <slot/>
    </h3>
  </Card>
</template>

<script>
import Card from "./Card.vue"

export default {
  components: {
    Card
  }
}
</script>