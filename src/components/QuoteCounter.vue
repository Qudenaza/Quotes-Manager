<template>
  <section class="quotes__counter">
    <h2 class="quotes__title">Quotes added</h2>
    <div class="quotes__bar">
      <span class="quotes__count">{{quotes.length}} / {{maxQuotes}}</span>
      <div class="quotes__line" :style="{'width': quotes.length + '0%'}"></div>
    </div>
  </section>
</template>

<script>
export default {
  props: ['quotes'],
  data: function() {
    return {
      maxQuotes: 10
    };
  }
};
</script>

<style>
.quotes__counter {
  padding: 2rem 2rem 4rem 2rem;
  font-family: 'Raleway', sans-serif;
}

.quotes__title {
  font-size: 2rem;
  margin-bottom: 2rem;
  text-align: left;
}

.quotes__bar {
  position: relative;
  height: 4rem;
  overflow: hidden;
  box-shadow: 0 0 1rem rgba(0, 0, 0, 0.3);
  background: #f1f1f1;
  border-radius: 1rem;
  text-align: center;
}

.quotes__count {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  font-size: 1.6rem;
}

.quotes__line {
  height: 100%;
  background-color: lightseagreen;
  transition: all 0.3s;
}
</style>

