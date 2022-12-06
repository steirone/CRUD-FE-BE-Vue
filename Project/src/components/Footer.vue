<template>
    <div class="p-5">
        <div class="d-flex justify-content-center">
            <img src="../assets/img/logo.png" alt="" />
        </div>
        <div class="d-flex justify-content-around mt-5">
            <div class="d-flex flex-column">
            <p class="font-weight-bold">Overview</p>
            <a class="text-dark mb-2" href="">Shipping</a>
            <a class="text-dark mb-2" href="">Refund</a>
            <a class="text-dark mb-2" href="">Promotion</a>
            </div>
            <div class="d-flex flex-column">
            <p class="font-weight-bold">Company</p>
            <a class="text-dark mb-2" href="">About</a>
            <a class="text-dark mb-2" href="">Carreer</a>
            <a class="text-dark mb-2" href="">Contact Us</a>
            </div>
            <div class="d-flex flex-column">
            <p class="font-weight-bold">Explore</p>
            <a class="text-dark mb-2" href="">Terms & Conds</a>
            <a class="text-dark mb-2" href="">Privay Policy</a>
            <a class="text-dark mb-2" href="">For Developer</a>
            </div>
            <div>
            <p class="font-weight-bold">Special Letter</p>
            <div class="input-group mb-3">
                <form action="" class="d-flex" id="specialLetterForm">
                <input
                    type="email"
                    class="form-control border-0 bg-light-grey"
                    id="specialLetterInput"
                    placeholder="Your email address"
                    style="width: 330px"
                    required
                />
                <button
                    type="submit"
                    class="btn bg-color-pink"
                    id="specialLetterButton"
                >
                    <img src="../assets/img/tele-icon.png" alt="" />
                </button>
                </form>
            </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "FooterComponent"
}
</script>

<style>
.bg-light-grey{
    background-color: #F9F9F9;
}

button.bg-color-pink{
    background-color: #F9CADA;
}

.border-radius-25{
    border-radius: 25px;
}

.border-color-pink{
    border: solid 2px #F9CADA;
}
</style>