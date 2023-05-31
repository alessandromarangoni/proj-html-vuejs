<script>
import section1 from './section1.vue';
import section2 from './section2.vue';
import section3 from './section3.vue';

export default {
    name: "mainSectionApp",
    components: {
        section1,
        section2,
        section3,
    }
}
</script>
<template>
    <!--container section1 cards -->
    <section1 />
    <!-- container 2 pseudojumbotron e cards-->
    <section2 />
    <!-- section 3 costumers -->
    <section3 />
</template>
<style scoped lang="scss">
@use '../style.scss'
</style>