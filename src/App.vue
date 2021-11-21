<template>
  <h1>Früchte Zähler</h1>
  <p>Gesamtanzahl an Früchten: {{ totalFruitCount }}</p>
  <div>
    <Counter title="Mango" emoji="🥭" @count-up="handleCount" />
    <Counter title="Äpfel" emoji="🍎" @count-up="handleCount" />
    <Counter title="Bananen" emoji="🍌" @count-up="handleCount" />
  </div>
</template>

<script>
import Counter from "./components/Counter.vue";
export default {
  name: "App",
  components: {
    Counter,
  },
  data() {
    return {
      totalFruitCount: 0,
    };
  },
  methods: {
    handleCount() {
      console.log("countup hier geht was ab");
    },
  },
};
</script>

<style>
body {
  font-family: Arial, Helvetica, sans-serif;
}
</style>
