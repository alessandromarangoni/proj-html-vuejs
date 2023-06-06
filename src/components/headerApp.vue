<script>
import jumbotronApp from './jumbotronApp.vue';
import logo from '../assets/logotype.png'
export default {
    name: "headerApp",
    components: {
        jumbotronApp
    },
    data() {
        return {
            windowTop: 0,
            HeaderColor: 'darker',
            logo: logo,
            headerLink: [{
                name: "Home",
                link: "7"
            }, {
                name: "about",
                link: "/"
            }, {
                name: "services",
                link: "/"
            }, {
                name: "projects",
                link: "/"
            }, {
                name: "blog",
                link: "/"
            }, {
                name: "contacts",
                link: "/"
            }],
        }
    }, mounted() {
        window.addEventListener("scroll", this.onScroll);
    },
    methods: {
        onScroll(e) {
            this.windowTop = e.target.documentElement.scrollTop;
        }
    }
}
// componente header che comprende logo e link di riferimento della pagina e componente jumbotron
</script>
<template>
    <header>
        <div class="container-fluid g-0 bg-alert" id="container">
            <div class=" pt-2 row justify-content-center fixed-top" :class="this.windowTop == 0 ? '' : this.HeaderColor">
                <div class="col-6">
                    <img :src="logo" alt="logo" class="logo">
                </div>
                <div class="col-5 bg-alert">
                    <ul class="d-flex justify-content-between text-right">
                        <li v-for="link in this.headerLink">
                            <a :href="link.link" class="text-white">{{ link.name }}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <jumbotronApp />
        </div>
    </header>
</template>
<style scoped lang="scss">
.logo {
    width: 80px;
}

.darker {
    background: rgb(0, 0, 0);
    background: linear-gradient(0deg, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 0.6629245448179272) 46%, rgba(0, 0, 0, 1) 88%);
}

li:hover {
    transform: scale(1.15);
}
</style>