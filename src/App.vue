<template>
  <div class="container">
    <img src="./assets/logo.png">
    <h2>Add Notes Here for Today</h2>
    <addNote @noteAdded="added"></addNote>
    <hr>
    <quotegrid :quotes="notesList" @removeNote="delNote"></quotegrid>
    <div class="row">
      <div class="col-sm-12 text center">
        <div class="alert alert-info text center">Click on quote to delete it!</div>
      </div>
    </div>

  </div>
</template>

<script>
  import grid from './components/quoteGrid.vue';
  import  Note from './components/newQuote.vue';
export default {
  data(){
    return{
      notesList : ['Find God in yourSelf'],
      notesLimit : 15
    }
  },
  components:{
    quotegrid : grid,
    addNote : Note
  },
  methods:{
    added(notes){
      this.notesList.push(notes)
    },
    delNote(index){
      console.log('here del')
      this.notesList.splice(index,1);

    }
  }

}
</script>

<style>

</style>
