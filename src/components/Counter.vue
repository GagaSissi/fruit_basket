<template>
  <article class="counter">
    <h2 class="counter__title">{{ title }}</h2>
    <div class="counter__action-area">
      <button class="counter__btn" @click="increase">+</button>
      <span class="counter__result">{{ result }}</span>
    </div>

    <p class="counter__emojis" v-if="this.emoji">{{ emojiCount }}</p>
  </article>
</template>

<script>
export default {
  name: "Counter",
  props: {
    title: {
      type: String,
      required: true,
    },
    emoji: {
      type: String,
      default: "",
    },
  },
  data() {
    return {
      result: 0,
    };
  },
  computed: {
    emojiCount() {
      if (!this.emoji) return;

      let count = 0;
      let emjoiList = "";
      while (count < this.result) {
        emjoiList += this.emoji;
        count++;
      }

      return emjoiList;
    },
  },
  methods: {
    increase() {
      this.result++;
    },
  },
};
</script>

<style scoped>
.counter {
  border: 1px solid rgb(186, 186, 186);
  border-radius: 5px;
  padding: 10px;
  margin-bottom: 10px;
  background: rgb(225, 225, 225);
}

.counter__btn,
.counter__result {
  font-size: 1.5rem;
}

.counter__result {
  display: inline-block;
  margin: 0 15px;
}
</style>
