<template>

    <!-- slide show container -->
    <div class="slideshow-container">

        <!-- Full-width images with number and caption text -->
        <div class="mySlides fade">
            <div class="numbertext">1 / 4</div>
            <img src="~/assets/images/img_lights_wide.jpg" style="width:100%">
            <div class="text">Caption One</div>
        </div>
                <div class="mySlides fade">
            <div class="numbertext">2 / 4</div>
            <img src="~/assets/images/img_mountains_wide.jpg" style="width:100%">
            <div class="text">Caption Two</div>
        </div>
                <div class="mySlides fade">
            <div class="numbertext">3 / 4</div>
            <img src="~/assets/images/img_nature_wide.jpg" alt="">
            <div class="text">Caption Three</div>
        </div>
                <div class="mySlides fade">
            <div class="numbertext">4 / 4</div>
            <img src="~/assets/images/img_snow_wide.jpg" alt="">
            <div class="text">Caption Four</div>
        </div>

        <!-- The dots/circles -->
        <div style="text-align:center">
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
        </div>

    </div>
</template>

<script>
export default {
    name: 'siteHeader'
}
</script>

<style lang="scss">

    .slideshow-container{
        border: 1px solid $green;
    }

</style>