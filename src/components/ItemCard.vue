<template>
    <div id="item-card">
        <div class="card" style="width: 18rem;">
        <img class="card-img-top" src="https://via.placeholder.com/350x150" alt="Card image cap">
        <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
            <a class="gumroad-button" :href="url" target="_blank">Subscribe</a>
        </div>
        </div>
    </div>
</template>
<script>
export default {
  name: "item-card",
  props:{
      url: String,
  },
  components: {},
};
</script>
<style>
  #item-card .gumroad-button{
    background-image: none !important;
  }
  #item-card .gumroad-button-logo{
    display: none !important;
  }
</style>
