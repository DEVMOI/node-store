<template>
<div id="ShopSlider" class="carousel slide" data-ride="carousel">
    <div class="carousel-inner">
        <div class="carousel-item active">
        <img class="d-block w-100" src="https://via.placeholder.com/350x150/000" alt="First slide">
        </div>
        <div class="carousel-item">
        <img class="d-block w-100" src="https://via.placeholder.com/350x150" alt="Second slide">
        </div>
        <div class="carousel-item">
        <img class="d-block w-100" src="https://via.placeholder.com/350x150/ert" alt="Third slide">
        </div>
    </div>
    <ol class="carousel-indicators">
        <li data-target="#ShopSlider" data-slide-to="0" class="active"></li>
        <li data-target="#ShopSlider" data-slide-to="1"></li>
        <li data-target="#ShopSlider" data-slide-to="2"></li>
    </ol>
</div>
</template>
<script>
export default {
    name:"slider",
}
</script>
