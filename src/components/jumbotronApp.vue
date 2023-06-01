<script>
export default {
    name: "jumbotronApp"
}
</script>

<template>
    <div class="jumbotron d-flex">
        <div class="jumbo_read_more_container position-relative">
            <div class="position-absolute jumbo_read_more">
                <div class=" ps-4  pt-3 d-flex align-items-center ">
                    <div class="small_separe"></div>
                    <span class="ps-2 text-white"> <small> ALWATS THE BEST WAY YOU NEED IT </small></span>
                </div>
                <h1 class="ps-4 pt-3  d-block text-white">THE BEST BUISNESS CONSULTING</h1>
                <div class="d-flex mt-3">
                    <div>
                        <button class="ms-4"><small>READ MORE</small></button>
                    </div>
                    <div class="text-white custom_border d-flex justify-content-center ms-3 align-items-center"><i
                            class="fa-solid fa-play"></i></div>
                </div>

            </div>
        </div>
        <div class="img-container">
            <img src="../assets/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg" alt="" class="">
        </div>
    </div>
</template>
<style scoped lang="scss">
@use'variables.scss' as *;

.jumbo_read_more_container {
    width: 40%;
    background-color: $mainColor;
    background-image: url(https://demo.phlox.pro/consulting-2/wp-content/uploads/sites/113/2019/06/Group_7543.svg);
    background-repeat: no-repeat;
    background-position-x: -5%;
    background-position-y: 290%;
    background-size: 60%;
    background-attachment: fixed;

    h1 {
        font-size: 55px;
    }

    button {
        background-color: $azule;
        border: 0;
        padding: .5rem 2rem;
        color: #13543f;
    }

    .jumbo_read_more {
        height: 350px;
        width: 500px;
        transform: translate(0, -50%);
        top: 50%;
        left: 40%
    }
}

small {
    font-size: .8rem;
}

.custom_border {
    height: 35px;
    width: 35px;
    border-radius: 50%;
    border: 2px solid $azule;
}

.img-container {
    width: 60%;

    img {
        width: 100%;
    }
}
</style>