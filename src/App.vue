<script>
import headerApp from './components/headerApp.vue';
import mainSectionApp from './components/mainSectionApp.vue';
import footerApp from './components/footerApp.vue';

export default {
  components: {
    headerApp,
    mainSectionApp,
    footerApp,
  }
}
</script>

<template>
  <headerApp />
  <mainSectionApp />
  <footerApp />
</template>

<style scoped></style>
