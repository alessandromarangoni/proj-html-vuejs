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
  <div class="message_icon_container d-flex justify-content-between align-items-center">
    <div class="return_up d-flex justify-content-center align-items-center"><a class="text-white" href="#container"><i
          class="fa-solid fa-arrow-up"></i></a></div>
    <div class="message_icon d-flex justify-content-center align-items-center">
      <i class="fa-regular fa-message"></i>
    </div>
  </div>
</template>

<style scoped lang="scss">
.message_icon_container {
  height: 100px;
  width: 100px;
  color: white;
  position: sticky;
  margin: -5.5rem 1rem;
  bottom: 0;
  left: 100%;

  .message_icon {
    height: 50%;
    width: 50%;
    border-radius: 50%;
    background-color: #527CEB;
  }

  .return_up {
    height: 40%;
    width: 40%;
    border-radius: 50%;
    background-color: rgb(154, 154, 154);
  }
}
</style>
