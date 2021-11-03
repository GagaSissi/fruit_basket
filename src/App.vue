<template>
  <h1>Früchte Zähler</h1>
  <p>Gesamtanzahl an Früchten: {{ totalFruitCount }}</p>
  <div>
    <Counter title="Mango" emoji="🥭" />
    <Counter title="Äpfel" emoji="🍎" />
    <Counter title="Bananen" emoji="🍌" />
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      totalFruitCount: 0,
    };
  },
};
</script>

<style>
body {
  font-family: Arial, Helvetica, sans-serif;
}
</style>