<script>
import image from '../assets/business-people-working-together-on-project-and-5FHSKBL.jpg'
export default {
    name: "section2",
    data() {
        return {
            image
        }
    }
}
</script>
<template>
    <section class="section_2">
        <div class="container-fluid">
            <div class="row">
                <div class="col-10">
                    <div class="row">
                        <div class="col-7 justify-content-center p-0">
                            <img :src="this.image" alt="" class="">
                        </div>
                        <div class=" col-5 bg-primary m-0">
                            <div>
                                <div></div>
                                <span></span>
                            </div>
                            <h4>placeHolder</h4>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem culpa iste aspernatur,
                                delectus
                                voluptas neque, est sunt nihil maiores consequuntur consequatur voluptatum qui veritatis vel
                                cupiditate modi hic dolorum animi!</p>
                        </div>
                    </div>
                    <div class="row position-relative">
                        <div class="col10 bg-secondary d-flex p-5 justify-content-center">
                            <div class="row d-flex p-5 justify-content-around">
                                <div class="col-3 d-flex align-items-center text-center">
                                    <h4>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</h4>
                                </div>
                                <div class="col-3 d-flex align-items-center text-center">
                                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aspernatur laboriosam esse
                                        quibusdam fuga blanditiis. Doloribus eius, corporis nesciunt perspiciatis, mollitia
                                        cupiditate magnam porro facere consequatur voluptate omnis nihil nam qui.</p>
                                </div>
                            </div>
                        </div>
                        <button class="position-absolute call-to-action">button</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style scoped lang="scss">
.call-to-action {
    width: 100px;
    right: 0;
    bottom: 0
}
</style>