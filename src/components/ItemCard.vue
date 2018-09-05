<template>
    <div id="item-card">
        <div class="card">
        <img class="card-img-top" :src="itemImage" :alt="itemImage" :title="itemDesc"/>
        <div class="card-body">
            <h5 class="card-title">{{itemName}}</h5>
            <h6>{{merchantName}}</h6>
            <p class="card-text">{{itemDesc.substring(0,40)}}...</p>
            <a class="gumroad-button w-100" :href="gumroadLink" target="_blank">{{buttonText}}</a>
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
      merchantName: String,
      itemDesc: String,
      gumroadLink: String,
      buttonText: String
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
