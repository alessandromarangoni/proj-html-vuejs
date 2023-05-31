<script>
import costumersImg1 from '../assets/oliver-ragfelt-488196-unsplash.jpg'
import costumersImg2 from '../assetS/12679.jpg'
import costumersImg3 from '../assets/oliver-ragfelt-488196-2.jpg'
import articleImg1 from '../assets/startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg'
import articleImg2 from '../assets/business-people-working-together-on-project-and-5FHSKBL-1390.jpg'
import imgLetsTalk from '../assets/startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg'
export default {
    name: "section3",
    data() {
        return {
            imgLetsTalk,
            costumerSays: [{
                img: costumersImg1,
                text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed by when I hear the buzz of the little.",
                name: 'Mark Hamilton',
                company: 'amazon inc'
            }, {
                img: costumersImg2,
                text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed by when I hear the buzz of the little.",
                name: 'Jhon Maxim',
                company: 'amazon inc'
            },
            {
                img: costumersImg3,
                text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed by when I hear the buzz of the little.",
                name: 'Vera Duncan',
                company: 'amazon inc'
            }],
            articles: [{
                img: articleImg1,
                date: 'july 4, 2019',
                author: 'by paul',
                title: 'Canadian Consulting Firm acquired by UK Giant',
                argument: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a ...'
            },
            {
                img: articleImg2,
                date: 'july 19, 2020',
                author: 'by paul',
                title: 'Canadian Consulting Firm acquired by UK Giant',
                argument: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a ...'
            }]
        }
    }

}
</script>
<template>
    <section>
        <div class="container">
            <div class="row d-flex justify-content-end">
                <div class="col-6 d-flex justify-content-end">
                    <span class="p-3">placeHolder</span>
                    <div class="p-3">------</div>
                </div>
            </div>
        </div>
        <div class="container-fluid">
            <div class="row d-flex justify-content-end">
                <div class="col-10 bg-primary">
                    <div class="d-flex justify-content-between">
                        <template v-for="item in this.costumerSays">
                            <div class="p-5 position-relative costumer_wrapper">
                                <div class="text_wrapper">
                                    <p> {{ item.text }}</p>
                                    <h4>{{ item.name }}</h4>
                                    <small>{{ item.company }}</small>
                                </div>
                                <img :src="item.img" alt="" class="img-fluid position-absolute costumer-img">
                            </div>
                        </template>
                    </div>
                </div>
            </div>
        </div>
        <div class="container">
            <div class="row d-flex justify-content-center">
                <div class="col-10 pt-5">
                    <div>
                        <div class="d-flex">
                            <div>---</div>
                            <span>placeHolder</span>
                        </div>

                        <div class="d-flex">
                            <h3>THE RECENT NEWS YOU MUST READ IT</h3>
                            <button>
                                button
                            </button>
                        </div>
                    </div>

                    <div class="d-flex justify-content-between mb-5">
                        <template v-for="item in this.articles">
                            <div class=" m-3 custom_container d-flex bg-primary position-relative flex-column
                                                                        align-items-end mb-5">
                                <img :src="item.img" alt="" class="img-fluid">
                                <div class="text_container bg-secondary position-absolute">
                                    <div>
                                        <span><small>{{ item.date }}</small></span>
                                        <span><small>{{ ' ' + item.author }}</small></span>
                                    </div>
                                    <h3>{{ item.title }}</h3>
                                    <p>{{ item.argument }}</p>
                                </div>
                            </div>
                        </template>
                    </div>
                </div>
            </div>
        </div>
        <div class="container-fluid pre-footer mt-5">
            <div class="row d-flex justify-content-center mt-5">
                <div class="col-6 mt-5 p-5 text-center">
                    <h3>LET'S TALK ABOUT WORK</h3>
                    <p>a wanderful serenity has taken possession Far far away. behind the word mountain</p>
                    <button>button</button>
                </div>
            </div>
        </div>
    </section>
</template>
<style scoped lang="scss">
.costumer_wrapper {
    width: calc(100% / 3);

    &:hover {
        .costumer-img {
            opacity: .5;
            z-index: 0;
        }

        .text_wrapper {
            width: 80%;
            position: absolute;
            color: white;
            z-index: 999;
        }
    }
}

.costumer-img {
    width: 350px;
    padding: .8rem;
    top: 0;
    left: 0;
    opacity: 0;
    z-index: 1;
}

.custom_container {
    width: calc(100%);


    .text_container {
        max-width: 80%;
        bottom: 0;
        transform: translate(0, 50%);
    }
}

.pre-footer {
    background-image: url('../assets/business-people-working-together-on-project-and-B3MZ4TX.jpg');
    background-size: cover;
}
</style>