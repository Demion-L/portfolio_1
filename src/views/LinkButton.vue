<template lang="">
  <div class="common-btn">
    <a target="_blanc" :href="link">{{ content }}</a>
  </div>
</template>
<script>
export default {
  props: {
    link: {
      type: String,
    },
    content: {
      type: String,
      required: true,
    },
  },
};
</script>
<style lang="scss" scoped>
.common-btn {
  padding: 0.5rem;
  max-width: 10rem;
  width: 100%;
  margin: 2rem auto;
  border-top: 1px solid rgb(245, 245, 240);
  border-left: 1px solid rgb(245, 245, 240);
  border-bottom: 1px solid rgba(18, 19, 18, 0.538);
  border-right: 1px solid rgba(18, 19, 18, 0.538);
  border-radius: 5px;
  backdrop-filter: blur(3px);
  cursor: pointer;
  a {
    color: #fff;
  }
}
</style>
