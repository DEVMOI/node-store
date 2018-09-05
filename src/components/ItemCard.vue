<template>
    <div id="item-card">
        <div class="card">
        <img class="card-img-top" :src="itemImage" :alt="itemImage">
        <div class="card-body">
            <h5 class="card-title">{{itemName}}</h5>
            <p class="card-text lead">{{itemDescription}}</p>
            <a class="gumroad-button w-100" :href="gumroadLink" target="_blank">{{gumroadLink}}</a>
        </div>
        </div>
    </div>
</template>
<script>
export default {
  name: "item-card",
  props:{
      itemImage: String,
      itemName: String,
      itemDescription: String,
      gumroadLink: String,
  }
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
