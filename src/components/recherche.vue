<template>
  <div class=“recherche”>
    <form class='container ' v-on:submit='bla'>
    <div class="form-group  col-lg-12 ">
      <input  col-lg-10 type="search" class="form-control" id="barre-recherche" v-model='titre'  placeholder="Breaking bad, Defender , Narco ....">
      <small id="textesearch" class="form-text text-muted">faite une recherche sur vos films et series preferées.</small>
      <button co-lg-2 type="submit" id='btn' class="btn btn-danger"></button>
    </div>
</form>

  </div>
</template>

<script>
export default {
  name:'recherche',
  data(){
    return {
      titre:''
    }
  },

methods : {
  bla(e){
    this.$emit('bla',this.titre)
    e.preventDefault()
  }
}
}
</script>

<!-- Add “scoped” attribute to limit CSS to this component only -->
<style scoped>
button {
  background : url('https://pbs.twimg.com/profile_images/744949842720391168/wuzyVTTX.jpg');
  background-repeat : no-repeat ;
  background-size : 100% 100%;
  height : 50px;
   width : 10%;

}
small {
  margin :2%;
}
h1 {
  color : white ;
}
</style>
