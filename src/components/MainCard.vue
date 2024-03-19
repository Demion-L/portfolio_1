<template lang="">
  <div class="main-container">
    <preview-block />
    <about-me />
  </div>
</template>

<script>
import PreviewBlock from "@/components/PreviewBlock.vue";
import AboutMe from "@/components/AboutMe.vue";

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

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (max-width: 768px) {
  .main-container {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}
</style>
