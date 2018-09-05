<template>
  <div id="store" class="Store">
    <ItemCard :url="subscription"></ItemCard>
    <ItemCard :url="google"></ItemCard>
  </div>
</template>

<script>
// @ is an alias to /src
import ItemCard from '@/components/ItemCard.vue'

export default {
  name: "store",
  components: {ItemCard},
  data(){
    return{
      subscription:"https://gum.co/Moikaship",
      google: "https://www.google.com"
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
