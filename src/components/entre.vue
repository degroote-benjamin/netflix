<template>
<div id="entre">
  <form v-on:submit="formsub">
    <input type="text" placeholder="entrer un titre" v-model="titre" class="input">
    <button type="submit" name="button">
      <img class="imglogo" src="http://vignette2.wikia.nocookie.net/logopedia/images/b/b2/NetflixIcon2016.jpg/revision/latest/scale-to-width-down/2000?cb=20160620223003" alt="">
    </button>
  </form>
</div>
</template>

<script>
export default {
  name: 'entre',
  data(){
    return {
      titre: ''
    }
  },
  methods: {
    formsub(e) {
      this.$emit('formsub',this.titre);
      e.preventDefault();
      $(".input").val("")
    }
  }
}
</script>

<style>
form{
  display: flex;
  justify-content: center;
  width: 100%;
  margin-top:30px;
}
input[type=text]{
  font-size: 35px;
  width: 70%;
}
button{
  height: 100px;
  width: 100px;
  padding: 0;
  background: black;
}
.imglogo{
  height: 100%;
  width: 100%;
}
</style>
