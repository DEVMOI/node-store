<template>
    <div id="item-card" class="w-100">
        <div class="card d-flex flex-md-row flex-xs-column w-100 my-2 bg-dark">
        <img class="card-img-top image-h p-0 rounded border border-dark mx-auto" :src="itemImage" :alt="itemImage" :title="itemDesc"/>
        <div class="bg-white card-body d-flex flex-column justify-content-between">
            <p class="lead card-title">{{itemName}}</p>
            <a class="gumroad-button w-100" :href="gumroadLink" target="_blank">{{btnText}}</a>
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
      btnText:String
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
  .image-h{
    height: 150px !important;
    width: 150px !important;
    max-width: 250px;
  }
</style>
