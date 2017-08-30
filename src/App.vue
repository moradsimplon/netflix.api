<template>
  <div id="app">

    <entete></entete>
    <recherche v-on:bla='netflix'></recherche>
    <affichage :someData='someData'></affichage>
  </div>
</template>

<script>
import entete from './components/entete'
import recherche from './components/recherche'
import affichage from './components/affichage'

export default {
  name: 'app',
  components: {
    entete,
    recherche,
    affichage
  },
data(){
  return{
    someData:''
  }
},

  methods : {
    netflix : function(titre){

    // GET /someUrl
    this.$http.get('http://netflixroulette.net/api/api.php?title='+titre).then(response => {
      // get body data
      this.someData = response.body;
      console.log(this.someData);


    }, response => {
      // error callback
    });

  }
  }
}
</script>

<style>
#app {

  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body{
    background-color : black;
}
</style>
