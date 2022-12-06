<template>
    <div class="bg-white p-4 border-radius-25">
        <a href="#" @click.prevent="$emit('changePicture', objCard.cardImage)">
            <img class="border-radius-25" 
                :src="require('@/assets/img/' + objCard.cardImage + '.png')" alt="" />
        </a>
        <p class="font-weight-bold mt-3 my-0">{{ objCard.cardTitle }}</p>
        <p>IDR {{ objCard.cardPrice }}</p>
    </div>
</template>

<script>
export default {
    name : "CardComponent",
    props : ["objCard"]
}
</script>

<style scoped>

</style>