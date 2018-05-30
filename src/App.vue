<template>
  <div class="container">
    <appNewQuote @quoteAdded='newQuote'></appNewQuote>
    <appQuoteGrid :quotes='quotes'></appQuoteGrid>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote.vue'

export default {
  data: function() {
    return {
      maxQuotes: 10,
      quotes: [
        'Just a quote to see something'
      ]
    };
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote
  }
}
</script>

<style>
</style>