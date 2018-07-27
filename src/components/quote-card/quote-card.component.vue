<template src="./quote-card.component.html"></template>
<style src="./quote-card.component.css"></style>

<script>
    import QuoteIcon from '../quote-icon/quote-icon.component.vue';
    import { Quote } from "./models/quote.model.js"
    export default {
        name: 'Quote-Card',
        data() {
            return {
                newQuote: 'New Quote',
                quote: {
                    quote: '',
                    author: ''
                }
            }
        },
        components: {
            QuoteIcon
        },
        methods: {
            getQuote: async function() {
                const response = await this.$http.get('https://talaikis.com/api/quotes/random/')
                const json = await response.json()
                this.quote = new Quote(json)
            }
        },
        created: function() {
            this.getQuote();
        }
    }
</script>

