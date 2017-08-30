<template>
<div id="app">
  <div class="img">
    <img src="https://truecostmovie.com/img/TTC/wp-content/uploads/2015/10/netflix_logo_digitalvideo-1.png" alt="">
  </div>
  <entre v-on:formsub="recupdata"></entre>
  <sortie v-bind:donner="donner"></sortie>
</div>
</template>

<script>
import Hello from './components/Hello'
import entre from './components/entre'
import sortie from './components/sortie'


export default {
  name: 'app',
  components: {
    entre,
    sortie
  },
  data() {
    return {
      donner: ''
    }
  },
  methods: {
    recupdata(titre) {
      // GET /someUrl
      this.$http.get('https://netflixroulette.net/api/api.php?title=' + titre)
        .then(response => {

          // get body data
          this.donner = response.body;
          console.log(this.donner)
        }, response => {
          // error callback
          console.log(titre);
        });
    }
  }
}
</script>

<style>
body {
  background: black;
}
.img{
  width: 100%;
  display:flex;
  justify-content: center;
}
.img img{
  width: 450px;
  height: 250px;
}
</style>
