<template>
  <section class="quotes">
    <quote-counter :quotes="quotes"></quote-counter>
    <quote-add :quotes="quotes"></quote-add>
    <quote-list :quotes="quotes"></quote-list>
  </section>
</template>

<script>
import QuoteCounter from './components/QuoteCounter';
import QuoteAdd from './components/QuoteAdd';
import QuoteList from './components/QuoteList';

export default {
  data: function() {
    return {
      quotes: []
    };
  },
  components: {
    quoteCounter: QuoteCounter,
    quoteAdd: QuoteAdd,
    quoteList: QuoteList
  }
};
</script>

<style>
*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

html {
  font-size: 62.5%;
}

body {
  box-sizing: border-box;
}

.quotes {
  padding: 2rem;
}
</style>
