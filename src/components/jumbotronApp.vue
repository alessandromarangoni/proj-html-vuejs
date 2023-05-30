<script>
export default {
    name: "jumbotronApp"
}
</script>

<template>
    <div class="jumbotron d-flex">
        <div class="jumbo_read_more_container position-relative">
            <div class="position-absolute jumbo_read_more">
                <span>placeHolder</span>
                <h1>placeHolder</h1>
                <button>button</button>
            </div>
        </div>
        <div class="img-container">
            <img src="../assets/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg" alt="" class="">
        </div>
    </div>
</template>
<style scoped lang="scss">
.jumbo_read_more_container {
    width: 40%;
    background-color: blue;

    // debug color
    .jumbo_read_more {
        height: 350px;
        width: 500px;
        background-color: red;
        transform: translate(0, -50%);
        top: 50%;
        left: 40%
    }
}

.img-container {
    width: 60%;

    img {
        width: 100%;
    }
}
</style>