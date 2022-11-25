<script setup>
import Card from "./components/Card.vue"
import TextCard from "./components/TextCard.vue"
import CounterCard from "./components/CounterCard.vue";
import RangeCard from "./components/RangeCard.vue";
import SearchCard from "./components/SearchCard.vue";
</script>

<template>
  <div class="components">
    <Card color="#fff8dd" title="Card Template"/>
    <TextCard color="#fff6f4" title="Sample text">
      Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's
      standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a
      type specimen book.
    </TextCard>
    <CounterCard color="#ebffda" title="Counter" :default-value="50"/>
    <RangeCard color="bisque" title="Range" :min="50" :max="150" :default-value="75"/>
    <SearchCard color="khaki" title="Search" :items="['bread', 'milk', 'burger', 'bike', '!@#$%^', 'mike']"/>
  </div>
</template>

<style scoped>
.components {
  display: flex;
  width: 100vw;
  height: 100vh;
  margin: 0;
  padding: 0;
  flex-wrap: wrap;
  align-items: flex-end;
  align-content: flex-start;
}
</style>
