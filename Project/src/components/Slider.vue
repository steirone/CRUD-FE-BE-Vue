<template>
    <div class="p-5 mt-5 bg-light-grey">
        <h3>Complete Your Room</h3>
        <h3>With What We Designed</h3>
        <div class="d-flex justify-content-between mt-4">
            <Card v-for="(item, index) in objCard" :key="index" :objCard="item" 
                @changePicture="changePictureFunc"></Card>
        </div>
    </div>
</template>

<script>
import Card from "./Card.vue"

export default {
    name: "SlideComponent",
    components : {
        Card
    },
    methods : {
        changePictureFunc : function(cardImage){
            // this.$emit('changePicture', cardImage)
            alert(cardImage)
        }
    },
    data() {
        return{
          objCard : [
            {
                cardTitle : "Cangkir Mauttie",
                cardPrice : "89.300.000",
                cardImage : "chair-1"
            },
            {
                cardTitle : "Saman Kakka",
                cardPrice : "14.500.000",
                cardImage : "chair-2"
            },
             {
                cardTitle : "Lino Dino",
                cardPrice : "22.000.000",
                cardImage : "chair-3"
            },
             {
                cardTitle : "Syail Ammeno",
                cardPrice : "12.000.000",
                cardImage : "chair-4"
            }
          ]
        }
    }
}
</script>

<style>

</style>