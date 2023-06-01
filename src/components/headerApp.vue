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
    }
}
// componente header che comprende logo e link di riferimento della pagina e componente jumbotron
</script>
<template>
    <header>
        <div class="container-fluid g-0 bg-alert" id="container">
            <div class="row justify-content-center fixed-top">
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
</style>