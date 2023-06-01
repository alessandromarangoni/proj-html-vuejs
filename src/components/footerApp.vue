<script>
import logo from '../assets/logotype-2-139x23.png'
export default {
    name: "footerApp",
    data() {
        return {
            logo,
            footerLink: [{
                name: "Home",
                link: "/"
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
            sociaLink: [{
                icons: 'fa-instagram',
                link: 'www.twitter.com'
            }, {
                icons: 'fa-linkedin',
                link: 'www.linkedin.com'
            }, {
                icons: ' fa-facebook',
                link: 'www.facebook.com'
            }, {
                icons: 'fa-twitter',
                link: 'www.twitter.com'
            }],
        }
    }
}
</script>
<template>
    <section>
        <div class="container">
            <div class="row">
                <div class="col ">
                    <div class="d-flex justify-content-between align-items-center">
                        <div><img :src="this.logo" alt=""></div>
                        <div>
                            <ul class="d-flex">
                                <li v-for="item in footerLink" class="p-2"><a :href="item.link">{{ item.name }}</a></li>
                            </ul>
                        </div>
                        <div>
                            <template v-for="items in sociaLink">
                                <span> <a href=""> <i class="fa-brands " :class="'' + items.icons"></i> </a></span>
                            </template>
                        </div>
                    </div>
                    <div class="footer_line mb-3"></div>
                    <div class="d-flex justify-content-between align-items-end">
                        <div>
                            <span class="d-block"><small><a href="">Term of use</a></small></span>
                            <span><small><a href="">Privacy Enviromental policy</a></small></span>
                        </div>
                        <div><span><small><a href="">Copyright © 2020 Phlox Consulting. All Rights
                                        Reserved.</a></small></span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style scoped lang="scss">
li {
    list-style: none;

    a {
        text-decoration: none;
    }
}

.footer_line {
    height: 1px;
    border: 1px solid black;
}
</style>