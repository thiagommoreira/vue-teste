<template>
  <div id="app">
    <Quote-Card></Quote-Card>
  </div>
</template>

<script>
import QuoteCard from './components/quote-card/quote-card.component.vue'

export default {
  name: 'app',
  components: {
    QuoteCard
  }
}
</script>

<style>
@import url('../node_modules/@fortawesome/fontawesome-free/css/all.css');

</style>
