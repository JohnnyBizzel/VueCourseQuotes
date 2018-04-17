<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <label>Quote</label>
                <textarea required class="form-control" rows="3" v-model="quote.txt"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <label>Author</label>
                <input type="text"  required  class="form-control" v-model="quote.author"></input>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
               <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
              quote: { txt: '',
                      author: ''}
            };
        },
        methods: {
            createNew() {
              // Todo: validation
                this.$emit('quoteAdded', this.quote);
                this.quote = { txt: '', author:''};
            }
        }
    }
</script>

<style>

</style>