<template>
    <div>
        <Navbar></Navbar>
        <Breadcrumbs></Breadcrumbs>
        <ShippingForm></ShippingForm>
        <SuccessForm class="d-none"></SuccessForm>
        <Footer></Footer>
    </div>
</template>

<script>
import Navbar from "../components/Navbar.vue"
import Breadcrumbs from "../components/Breadcrumbs.vue"
import ShippingForm from "../components/ShippingForm.vue"
import Footer from "../components/Footer.vue"
import SuccessForm from "../components/SuccessForm.vue"

export default {
    name: "ShippingPage",
    components: {
        Navbar,
        Breadcrumbs,
        ShippingForm,
        Footer,
        SuccessForm
    }
}
</script>

<style>

</style>