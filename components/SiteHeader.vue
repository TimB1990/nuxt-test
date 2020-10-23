<template>
    <div>
        <p>
            <a @click="prev">Previous</a> || <a @click="next">Next</a>
        </p>
        <transition-group name='fade' tag='div'>
            <div v-for="number in [currentNumber]" :key="number">
                <img :src="images[Math.abs(currentNumber) % images.length]" @mouseover="stopSlider" @mouseout="startSlider">
            </div>
        </transition-group>     
    </div>
</template>

<script>
export default {
    name: 'siteHeader',
    data(){
        return {
            images: [
                "/images/img_lights_wide.jpg",
                "/images/img_mountains_wide.jpg",
                "/images/img_nature_wide.jpg",
                "/images/img_snow_wide.jpg"
            ],
            currentNumber: 0,
            timer: null
        }
    },

    mounted(){
        this.startSlider()
    },

    methods: {
        startSlider(){
            this.timer = setInterval(this.next, 3000);
        },

        stopSlider(){
            clearTimeout(this.timer)
            this.timer = null
        },

        next(){
            this.currentNumber += 1
            console.log(this.currentNumber)
        },
        prev(){
            this.currentNumber -= 1;
            console.log(this.currentNumber)
        }
    }
}
</script>

<style lang="scss">

.fade-enter-active, .fade-leave-active {
 transition: all 0.8s ease;
 overflow: hidden;
 visibility: visible;
 opacity: 1;
 position: absolute;
}
.fade-enter, .fade-leave-to {
 opacity: 0;
 visibility: hidden;
}


</style>