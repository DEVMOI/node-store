<template>
  <div id="store" class="store">
    <ShopSlider></ShopSlider>
    <div class="col-lg-4">
      <ItemCard :gumroadLink="url"></ItemCard>
    </div>
  </div>
</template>

<script>
import axios from "axios";
// @ is an alias to /src
import ItemCard from '@/components/ItemCard';
import ShopSlider from "@/components/ShopSlider";

export default {
  name: "store",
  components: {
    ItemCard,
    ShopSlider
  },
  data(){
    return{
      itemImage: null,
      itemName: null,
      itemDesc: null,
      merchantName: null,
      url: null
    }
  }
};
</script>
<style>
  #store .gumroad-button{
    background-image: none !important;
  }
  #store .gumroad-button-logo{
    display: none !important;
  }
</style>
