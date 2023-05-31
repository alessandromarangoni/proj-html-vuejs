<script>
import costumersImg1 from '../assets/oliver-ragfelt-488196-unsplash.jpg'
import costumersImg2 from '../assetS/12679.jpg'
import costumersImg3 from '../assets/oliver-ragfelt-488196-2.jpg'
export default {
    name: "section3",
    data() {
        return {
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
</style>