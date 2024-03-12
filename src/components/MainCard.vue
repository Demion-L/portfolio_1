<template lang="">
  <div class="main-container">
    <preview-block />
    <about-me />
  </div>
</template>

<script>
import PreviewBlock from "./PreviewBlock.vue";
import AboutMe from "./AboutMe.vue";

export default {
  components: {
    PreviewBlock,
    AboutMe,
  },
};
</script>

<style scoped lang="scss">
.main-container {
  display: flex;
  background: url("../assets/main\ bg/code.jpg");
}
</style>
