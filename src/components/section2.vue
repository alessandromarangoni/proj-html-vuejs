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
            iLeft: 0,
            iCenter: 1,
            iRight: 2,
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
            }, {
                img: 'https://picsum.photos/790/592',
                imgHover: hoverimage1,
                title: 'Purinky ',
                category: 'uncategorized'
            }, {
                img: 'https://picsum.photos/790/592',
                imgHover: hoverimage1,
                title: ' product',
                category: 'uncategorized'
            }],
        }
    }, methods: {
        nextCard() {
            this.iLeft++
            this.iCenter++
            this.iRight++
            if (this.iRight >= this.cardSlider.length) {
                this.iLeft = 0,
                    this.iCenter = 1,
                    this.iRight = 2
            }
        },
        prevCard() {
            this.iLeft--
            this.iCenter--
            this.iRight--
            if (this.iRight < 2) {
                this.iLeft = (this.cardSlider.length - 3),
                    console.log(this.iLeft)
                this.iCenter = (this.cardSlider.length - 2),
                    console.log(this.iCenter)
                this.iRight = this.cardSlider.length - 1
                console.log(this.iRight)
            }
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
                        <div class=" col-5 d-flex flex-column justify-content-center align-items-start ps-3 m-0">
                            <div class="d-flex align-items-center ps-3">
                                <div class="small_separe"></div>
                                <span class="ps-3 text-white"><small>ABOUT US</small></span>
                            </div>
                            <h1 class="text-white p-3">WE MAKE YOUR STRATEGY WORK</h1>
                            <p class="text-white p-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem culpa
                                iste aspernatur,
                                delectus
                                voluptas neque, est sunt nihil maiores consequuntur consequatur voluptatum qui veritatis vel
                                cupiditate modi hic dolorum animi!</p>
                        </div>
                    </div>
                    <div class="row position-relative">
                        <div class="col10 d-flex justify-content-center call_to_action_container">
                            <div class="row d-flex justify-content-around p-4">
                                <div class="col-4  p-3 d-flex align-items-center text-center">
                                    <h4>WE HELP TO DELIVER THE BUISNESS CASE</h4>
                                </div>
                                <div class="col-4 p-3 d-flex align-items-center text-center">
                                    <p> <small>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aspernatur
                                            laboriosam esse
                                        </small>
                                    </p>
                                </div>
                            </div>
                        </div>
                        <button class="position-absolute call-to-action"><small>GET STARTED</small></button>
                    </div>
                </div>
            </div>
        </div>
        <div class="container">
            <div class="row pt-5">
                <div class="col-10 pt-5">
                    <div class="d-flex">
                        <div class="small_separe"></div><span class="ms-3 text-white"><small>PROJECT</small> </span>
                    </div>
                    <div class="d-flex justify-content-between">
                        <h4 class="text-white pt-3">OUR EXPERT TRUSTED CONSULTANT <br>HELP CLIENT</h4>
                        <div class="">
                            <button><i class="fa-solid fa-arrow-left" @click="prevCard()"></i></button>
                            <button class="ms-3" @click="nextCard"><i class="fa-solid fa-arrow-right"></i></button>
                        </div>
                    </div>
                    <div class="d-flex justify-contet-between ">
                        <div v-for="(item, i) in this.cardSlider"
                            :class="i == this.iLeft | i == this.iCenter | i == this.iRight ? 'd-block' : 'd-none'">
                            <div class=" position-relative card_wrapper p-3">
                                <div class="position-absolute item">
                                    <img :src="item.img" alt="" class="item_size">
                                    <div class="card_pos">
                                        <h3 class="text-white ps-3">{{ item.title }}</h3>
                                        <span class="text-white ps-3 pb-3 d-block">{{ item.category }}</span>
                                    </div>
                                </div>
                                <div class="">
                                    <img :src="item.imgHover" alt="" class="item_hover_size">
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
@use'variables.scss' as *;

.section_2 {
    background-color: $mainColor;
    background-image: url(https://demo.phlox.pro/consulting-2/wp-content/uploads/sites/113/2019/06/Group_7543.svg);
    background-size: contain;
    background-position-x: right;
    background-position-y: -170%;
    background-size: 60%;
    background-repeat: no-repeat;
}

.call_to_action_container {
    background-color: $azule;
}

.call-to-action {
    max-width: 200px;
    right: 0;
    bottom: 0;
    border: 0;
    color: white;
    background-color: #F81D39;
    padding: 0.5rem 1.5rem;
}

button {
    border: 1px solid rgb(255, 149, 0);
    padding: .5rem .8rem;
    background-color: $mainColor;

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

.item_hover_size {
    width: 105%;
    height: 105%;
}
</style>