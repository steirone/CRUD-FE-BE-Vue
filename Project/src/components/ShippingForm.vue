<template>
    <div class="row justify-content-center mt-4">
        <div class="col-6">
            <!-- Form Section -->
            <form class="border-color-pink rounded p-5" @submit.prevent="inputShipping" v-show="!success">
                <h2 class="text-center mb-4">Shipping Form</h2>
                <div class="row">
                    <div class="col-6">
                        <div class="form-group">
                            <label for="exampleInputEmail1">First Name</label>
                            <input
                                v-model="shippingData.first_name"
                                type="text"
                                class="form-control"
                                placeholder="Enter your first name"
                                required
                            />
                        </div>
                        <div class="form-group">
                            <label for="exampleInputEmail1">Last Name</label>
                            <input
                                v-model="shippingData.last_name"
                                type="text"
                                class="form-control"
                                placeholder="Enter your last name"
                                required
                            />
                        </div>
                        <div class="form-group">
                            <label for="exampleInputEmail1">Email address</label>
                            <input
                                v-model="shippingData.email"
                                type="email"
                                class="form-control"
                                placeholder="Enter email"
                                required
                            />
                        </div>
                    </div>
                    <div class="col-6">
                        <div class="form-group">
                            <label for="exampleInputEmail1">Phone Number</label>
                            <input
                            v-model="shippingData.phone_number"
                                type="number"
                                class="form-control"
                                placeholder="Enter phone number"
                                required
                            />
                        </div>
                        <div class="form-group">
                            <label for="exampleInputEmail1">City</label>
                            <input
                                v-model="shippingData.city"
                                type="text"
                                class="form-control"
                                placeholder="Enter city"
                                required
                            />
                        </div>
                        <div class="form-group">
                            <label for="exampleInputEmail1">Postal Code</label>
                            <input
                                v-model="shippingData.postal_code"
                                type="number"
                                class="form-control"
                                placeholder="Enter postal code"
                                required
                            />
                        </div>
                    </div>
                </div>
                <div class="form-group">
                    <label for="exampleFormControlTextarea1">Address</label>
                    <textarea
                        v-model="shippingData.address"
                        class="form-control"
                        rows="3"
                        placeholder="Enter address"
                        required
                    ></textarea>
                </div>

                <button type="submit" class="btn bg-color-pink">{{ buttonValue }}</button>
            </form>

            <!-- Success Section -->
            <SuccessForm v-show="success"></SuccessForm>

        </div>
    </div>
</template>

<script>
    import shippingService from "../services/shippingService.js"
    import SuccessForm from "./SuccessForm.vue"

    export default {
        data(){
            return{
                shippingData:{
                    "first_name" : null,
                    "last_name" : null,
                    "email" : null,
                    "phone_number" : null,
                    "city" : null,
                    "postal_code" : null,
                    "address" : null
                },
                success : false,
                buttonValue : "Submit"
            }
        },
        methods : {
            inputShipping(){
                let data = this.shippingData;

                if(this.buttonValue === "Submit"){
                    shippingService.create(data)
                        .then(response => {
                            console.log(response.data);
                            this.success = true;
                        })
                        .catch(e => {
                            console.log(e);
                        });
                }else{
                    shippingService.updateShipping(data.id, data)
                        .then(response => {
                            console.log(response.data);
                            this.success = true;
                        })
                        .catch(e => {
                            console.log(e);
                        });
                }
            },
        },
        components : {
            SuccessForm
        },
        props: ["shippingDataProps"],
        watch: {
            'shippingDataProps'(newValue) {
                this.shippingData = newValue;
                console.log(this.shippingData);
                this.buttonValue = "Update"
            }
        }
    }
</script>

<style scoped>
.border-radius-25{
    border-radius: 25px;
}

.border-color-pink{
    border: solid 2px #F9CADA;
}
</style>