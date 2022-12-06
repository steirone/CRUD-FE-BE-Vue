<template>
    <div>
        <Navbar></Navbar>
        <Breadcrumbs></Breadcrumbs>
        <Gallery class="mt-5" :galleryImage="galleryImage"></Gallery>
        <Slider @changePicture="changePictureFunc"></Slider>
        <Footer></Footer>
        <Copyright></Copyright>
    </div>
</template>

<script>
    import Navbar from "../components/Navbar.vue"
    import Breadcrumbs from "../components/Breadcrumbs.vue"
    import Gallery from "../components/Gallery.vue"
    import Slider from "../components/Slider.vue"
    import Footer from "../components/Footer.vue"
    import Copyright from "../components/Copyright.vue"

    export default {
        name: 'HomePage',
        components : {
            Navbar, Breadcrumbs, Gallery, Slider, Footer, Copyright
        },
        methods : {
            changePictureFunc : function(cardImage){
            this.galleryImage = cardImage
            },
        },
        data(){
            return{
                galleryImage : "chair"
            }
        }
    }
</script>

<style>

</style>