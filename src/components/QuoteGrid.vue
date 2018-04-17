<template>
  <div class="container">
    <div class="row">
        <app-quote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">
          <div class="textLarger" slot="content">{{ quote.txt }}</div>
          <span slot="content">{{ quote.author }}</span>
        </app-quote>
    </div>
  </div>    
</template>

<script>
    import Quote from './Quote.vue';

    export default {
        props: ['quotes'],
        components: {
            appQuote: Quote
        },
        methods: {
            deleteQuote(index) {
                this.$emit('quoteDeleted', index);
            }
        }
    }
</script>

<style>
.textLarger {
  font-size: 1.5em;
}
</style>