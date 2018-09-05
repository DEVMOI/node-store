<template>
  <div id="store" class="js-store">
    <!-- <ShopSlider></ShopSlider> -->
    <div class="mt-3" v-for="stock in stocks" :key="stock.id">
      <div class="col-lg-3" >
        <ItemCard :itemImage="stock.itemImage"
        :itemName="stock.itemName" :itemDesc="stock.itemDesc"
        :merchantName="stock.merchantName" :gumroadLink="stock.gumroadLink"
        :buttonText="stock.buttonText"></ItemCard>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
// @ is an alias to /src
import ItemCard from '@/components/ItemCard';
import ShopSlider from "@/components/ShopSlider";

const api = "https://cdn.rawgit.com/NodeGG/node-store/element/itemcard/src/data/Stock.json";
const gumScript = "https://gumroad.com/js/gumroad.js";

export default {
  name: "store",
  components: {
    ItemCard,
    ShopSlider
  },
  data(){
    return{
      stocks: []
    };
  },
  mounted() {
    let gumRoadScript = document.createElement("script");
    gumRoadScript.setAttribute("src", gumScript);
    document.body.appendChild(gumRoadScript);

    axios
      .get(api) 
      .then(res => {
        res = res.data.stock;     
        this.stocks = res;
      })
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
