<template>
    <div>
        <Navbar></Navbar>
        <Breadcrumbs></Breadcrumbs>
        <div class="row justify-content-center">
            <div class="col-10">
                <ShippingListTable v-show="!viewForm" @updateShippingFunc="updateShippingFunc"></ShippingListTable>
                <ShippingForm v-show="viewForm" :shippingDataProps="shippingData"></ShippingForm>
            </div>
        </div>
        <Footer class="mt-4"></Footer>
        <Copyright></Copyright>
    </div>
</template>

<script>
    import Navbar from "../components/Navbar.vue"
    import Breadcrumbs from "../components/Breadcrumbs.vue"
    import Footer from "../components/Footer.vue"
    import Copyright from "../components/Copyright.vue"
    import ShippingListTable from "../components/ShippingListTable.vue"
    import ShippingForm from "../components/ShippingForm.vue"

    export default {
        name: "ShippingList",
        components: {
            Navbar, 
            Breadcrumbs,
            Footer,
            Copyright,
            ShippingListTable,
            ShippingForm
        },
        methods: {
            updateShippingFunc(item){
                this.shippingData = item
                this.viewForm = true;
            }
        },
        data(){
            return{
                viewForm : false,
                shippingData: null
            }
        }
    }
</script>

<style>

</style>