<template>
    <div class="d-flex pl-5 bg-light-grey py-4 mt-4">
        <router-link to="/home" class="nav-link text-dark">Home</router-link>
        <span class="nav-link" v-show="currentRouteName == '/shipping'">/</span>
        <router-link to="/shipping" v-show="currentRouteName == '/shipping'" class="nav-link text-dark">Shipping</router-link>
        <span class="nav-link" v-show="currentRouteName == '/shippingList'">/</span>
        <router-link to="/shippingList" v-show="currentRouteName == '/shippingList'" class="nav-link text-dark">Shipping List</router-link>
    </div>
</template>

<script>
export default {
    name: "BreadcrumbsComponent",
    computed: {
        currentRouteName() {
            return this.$route.path
        }
    },
}
</script>

<style scoped>
    .router-link-active{
        font-weight: 600;
    }
</style>