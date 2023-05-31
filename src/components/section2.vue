<script>
import image from '../assets/business-people-working-together-on-project-and-5FHSKBL.jpg'
import expertImage1 from '../assets/DRY-1-790x592.jpg'
import expertImage2 from '../assets/221bf0b7-8134-43bb-936a-5acbe42db64a-790x592.jpg'
import expertImage3 from '../assets/z1el4c4p-790x592.jpg'
import hoverimage1 from '../assets/dry-red.jpg'
import hoverimage2 from '../assets/proposalRed.jpg'
import hoverimage3 from '../assets/templateRed.jpg'
export default {
    name: "section2",
    data() {
        return {
            image,
            cardSlider: [{
                img: expertImage1,
                imgHover: hoverimage1,
                title: 'Purinky product',
                category: 'uncategorized'
            }, {
                img: expertImage2,
                imgHover: hoverimage2,
                title: 'Purinky product',
                category: 'uncategorized'
            },
            {
                img: expertImage3,
                imgHover: hoverimage3,
                title: 'Purinky product',
                category: 'uncategorized'
            }],
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
                            <img :src="this.image" alt="" class="img-fluid">
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
        <div class="container">
            <div class="row">
                <div class="col-10">
                    <div class="d-flex">
                        <div>---</div><span>testo</span>
                    </div>
                    <div class="d-flex justify-content-between">
                        <h3>placeHolder</h3>
                        <div class="">
                            <button> left</button>
                            <button>right</button>
                        </div>
                    </div>
                    <div class="d-flex justify-contet-between ">
                        <div v-for="item in this.cardSlider">
                            <div class="position-relative card_wrapper p-3">
                                <div class="position-absolute item">
                                    <img :src="item.img" alt="" class="item_size">
                                    <div class="card_pos">
                                        <h3 class="">{{ item.title }}</h3>
                                        <span class="">{{ item.category }}</span>
                                    </div>
                                </div>
                                <div>
                                    <img :src="item.imgHover" alt="" class=" item_size">
                                </div>
                            </div>
                        </div>
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

.card_wrapper {
    max-width: 390px;

    img: {
        width: 390px;
    }

    img:hover {
        opacity: 0;
    }

    .item:hover {
        img: {
            opacity: 0;
        }

        .card_pos {
            opacity: 1
        }
    }

    .card_pos {
        bottom: 0;
        position: absolute;
        line-height: 3rem;
        opacity: 0;
    }
}

.item_size {
    width: 100%;
    height: 100%;
}
</style>