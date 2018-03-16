<template>
  <div class="row">
    <app-quote v-for="(q,index) in quotes" @click.native="delnote(index)">{{q}}</app-quote>


  </div>

</template>

<script>
  import Quote from './Quote.vue'
    export default {
      props:['quotes'],
      components:{
        appQuote : Quote
      },
      methods:{
        delnote(index){
          this.$emit('removeNote',index)
        }
      }


    }
</script>

<style scoped>

</style>
