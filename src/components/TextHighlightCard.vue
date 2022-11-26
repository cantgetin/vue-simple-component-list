<template>
  <Card>
    <div hidden ref="slotWrapper">
      <slot></slot>
    </div>
    <input type="text" placeholder="enter text" v-model="searchString"/>
    <h3 class="text" v-html="getHighlightedText(this.text, searchString)">
    </h3>
  </Card>
</template>

<script>
import Card from "./Card.vue"

export default {
  components: {
    Card
  },
  data() {
    return {
      text: "",
      searchString: ""
    }
  },
  mounted() {
    this.text = this.$refs.slotWrapper.innerText;
  },
  methods: {
    getHighlightedText(text, query) {
      if (query !== '') {
        let check = new RegExp(query, "ig");
        return text.toString().replace(check, function (matchedText, a, b) {
          return ('<b style="background: black; color: white;">' + matchedText + '</b>');
        });
      } else return text;
    },
  }
}
</script>

<style scoped>
.text {
  margin: 10px 0;
}
</style>