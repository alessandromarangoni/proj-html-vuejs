<script>
export default {
    name: "section1",
    data() {
        return {
            cards: [{
                title: 'STATICAL CONSULTING',
                img: 'missing',
                text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a'
            }, {
                title: 'DIGITAL CONSULTING',
                img: 'missing',
                text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a'
            }, {
                title: 'BANKING CONSULTING',
                img: 'missing',
                text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a'
            }, {
                title: 'ENTERPRICE CONSULTING',
                img: 'missing',
                text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a'
            }]
        }
    }
}
</script>
<template>
    <div class="container m-5">
        <div class="row justify-content-end">
            <div class="col-4 d-flex justify-content-end">
                <span>
                    placeHolder
                </span>
            </div>
            <div class="col-6">
                --------------------------------------------------------------------
            </div>
        </div>
    </div>
    <div class="container mt-5">
        <div class="row d-flex justify-content-between flex-wrap pb-5">
            <div class="col-12 d-flex flex-wrap pb-5">
                <template v-for="card in this.cards ">
                    <div class="d-flex card_items align-items-start">
                        <div class="img-wrapper m-2 me-4"></div>
                        <div class="p-2">
                            <h4 class="pt-2">{{ card.title }}</h4>
                            <p class="pe-4 card_text">{{ card.text }}</p>
                        </div>
                    </div>
                </template>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
.card_items {
    width: 50%;
}

.img-wrapper {
    min-width: 50px;
    height: 50px;
    background-color: red;
    border-radius: 50%;
}

.card_text {
    max-width: 80%;
}
</style>