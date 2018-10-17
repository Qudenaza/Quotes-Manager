<template>
  <section class="quotes__list">
    <div class="quotes__quote" v-for="(quote, id) in quotes" :key="id" @click="deleteQuote(id)">{{quote}}</div>
  </section>
</template>

<script>
export default {
  props: ['quotes'],
  methods: {
    deleteQuote(id) {
      this.quotes.splice(id, 1);
    }
  }
};
</script>

<style>
.quotes__list {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  margin-top: 2rem;
  border: 1px solid #f1f1f1;
  border-radius: 5px;
}

.quotes__quote {
  padding: 2rem;
  margin-bottom: 2rem;
  font-family: 'Open Sans', sans-serif;
  padding: 1rem;
  background: lightseagreen;
  border-radius: 5px;
  box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.5);
  font-size: 1.6rem;
  cursor: pointer;
}
</style>

