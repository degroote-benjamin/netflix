<template>
<div id="sortie" class="container">
  <div class="row">
    <div class="col-6">
      <img :src="donner.poster" alt="" class="col-12">
    </div>
    <div class="col-6 text-center">
      <h2 class="col-12">{{donner.show_title}}</h2>
      <p class="my-2">{{donner.summary}}</p>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'sortie',
  props: ['donner']
}
</script>

<style>
#sortie {
  color: white;
  margin-top:25px;
}
</style>
