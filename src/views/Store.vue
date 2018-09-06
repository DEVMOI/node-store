<template>
  <div id="store" class="js-store">
    <!-- SLIDER -->
    <div class="mb-3 pb-1">
      <!-- <ShopSlider></ShopSlider> -->
    </div>
    
    <!-- Searchbar -->
    <div class="my-2">
      <!-- <Searchbar class=" w-50" @emitinput="filteredList" /> -->
      </div>
    <!-- STORE -->
    <div class="mt-3 d-flex flex-column container">
      <div class="" v-for="stock in stocks" :key="stock.id">
        <ItemCard :itemImage="stock.itemImage"
        :itemName="stock.itemName" :itemDesc="stock.itemDesc"
        :merchantName="stock.merchantName" :gumroadLink="stock.gumroadLink"
        :btnText="btnText"></ItemCard>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
// @ is an alias to /src
import ItemCard from '@/components/ItemCard';
import ShopSlider from "@/components/ShopSlider";
import Searchbar from "@/components/Searchbar";

const api = "https://cdn.rawgit.com/NodeGG/node-store/3862312e/src/data/Stock.json";
// use this for dev https://rawgit.com/NodeGG/node-store/dev/src/data/Stock.json
const gumScript = "https://gumroad.com/js/gumroad.js";

export default {
  name: "store",
  components: {
    ItemCard,
    ShopSlider,
    Searchbar
  },
  data(){
    return{
      btnText: "Click For More!",
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
  },
   methods: {
    filteredList(eveny) {
      console.log(this.stocks);
      console.log(event)
      return this.stocks.filter(stock => {
        return stock.itemName.toLowerCase().includes(this.search.toLowerCase())
      })
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
