<template>
  <section class="quotes__add">
    <h3 class="quotes__title quotes__title--small">Quote</h3>
    <form class="quotes__form" @submit.prevent="addQuote">
      <textarea class="quotes__text" name="quote" v-model="quote"></textarea>
      <button class="quotes__btn" type="submit">Add</button>
    </form>
  </section>
</template>

<script>
export default {
  props: ['quotes'],
  data: function() {
    return {
      quote: ''
    };
  },
  methods: {
    addQuote() {
      if (this.quotes.length === 10) {
        alert('Больше добавлять нельзя!');

        return;
      }

      if (this.quote) {
        this.quotes.push(this.quote);

        this.quote = '';
      }
    }
  }
};
</script>

<style>
.quotes__add {
  padding: 2rem;
  border-top: 2px solid #f1f1f1;
  border-bottom: 2px solid #f1f1f1;
}

.quotes__title--small {
  margin-bottom: 1rem;
  text-align: center;
  font-size: 1.6rem;
}

.quotes__form {
  width: 70%;
  margin: 0 auto;
  text-align: left;
}

.quotes__text {
  display: block;
  width: 100%;
  padding: 1rem;
  font-family: 'Raleway', sans-serif;
  border: 1px solid grey;
}

.quotes__btn {
  width: 100%;
  padding: 1rem 2rem;
  margin-top: 2rem;
  background: cadetblue;
  border: none;
  font-weight: bold;
  border-radius: 2px;
  transition: background 0.2s;
  font-family: 'Raleway', Courier, monospace;
}

@media (min-width: 600px) {
  .quotes__btn {
    width: 50%;
  }
}

@media (min-width: 800px) {
  .quotes__btn {
    width: 30%;
  }
}

.quotes__btn:hover {
  cursor: pointer;
  background: lightseagreen;
}
</style>
