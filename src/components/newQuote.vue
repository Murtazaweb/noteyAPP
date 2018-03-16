<template>
<div class="row">
  <form>
    <div class="col-sm-8 col-sm-offset-2">
      <label>Notes</label>
      <textarea class="form-control" v-model="note"></textarea>
    </div>
    <div class="col-sm-8 col-sm-offset-2">
      <button class="btn btn-primary" @click.prevent="newNote">Add new Note</button>

    </div>
  </form>
</div>
</template>

<script>
    export default {
      data(){
        return{
          note:''
        }
      },
      methods:{
        newNote(){
          this.$emit('noteAdded', this.note);
          this.note = ''
        }
      }
    }
</script>

<style scoped>

</style>
