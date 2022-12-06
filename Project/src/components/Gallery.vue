<template>
    <div class="px-5">
        <div class="d-flex">
            <div class="d-flex flex-column justify-content-between mr-3">
                <img class="border-radius-25" src="../assets/img/side-1.png" alt="" />
                <img class="border-radius-25" src="../assets/img/side-2.png" alt="" />
                <img class="border-radius-25" src="../assets/img/side-3.png" alt="" />
                <img class="border-radius-25" src="../assets/img/side-1.png" alt="" />
                <img class="border-radius-25" src="../assets/img/side-2.png" alt="" />
            </div>
            <div class="mr-5">
                <img
                    class="border-radius-25"
                    :src="require('@/assets/img/' + galleryImage + '.png')"
                    alt=""
                    id="mainImage"
                />
            </div>
            <div class="py-4">
                <h1>Chair Thatty</h1>
                <p>IDR 12.000.000</p>
                <a
                    href="shippingPage.html"
                    class="btn font-weight-bold text-dark"
                    style="width: 230px; border-radius: 57px"
                >
                    <span class="mr-3">
                    <img src="../assets/img/cart-icon.png" alt="" />
                    </span>
                    Add to cart
                </a>
                <hr />
                <p class="font-weight-bold mt-4">About the product:</p>
                <p>
                    Tailored to a level of perfection synonymous with that of a Savile
                    Row suit and with understated quality in the detail, Jetty has
                    been influenced by timeless 1950s style.
                </p>
                <p>
                    Providing a subtle nod to the past, Jetty also provides a perfect
                    solution for the way we work today. A comprehensive product
                    family, Jetty features a variety of elegant chairs and sofas.
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name : 'GalleryComponent',
    props : ["galleryImage"] 
}
</script>

<style scoped>
    div a{
        background-color: #F9CADA;
    }
</style>