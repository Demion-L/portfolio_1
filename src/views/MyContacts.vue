<template lang="">
  <div class="contacts-container">
    <ul>
      <li>Telephone: <a href="tel:+358 41 793 68 35">+358 41 793 68 35</a></li>
      <li>Email: <a href="mailto:pradovd4@gmail.com">pradovd4@gmail.com</a></li>
    </ul>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.contacts-container {
  margin: 1rem 2rem;
  background: linear-gradient(
    126deg,
    rgba(249, 231, 38, 1) 0%,
    rgba(196, 232, 134, 1) 25%,
    rgba(3, 123, 148, 1) 100%
  );
  border-radius: 5px;
  border-top: 1px solid rgb(245, 245, 240);
  border-left: 1px solid rgb(245, 245, 240);
  border-bottom: 1px solid rgba(47, 59, 49, 0.782);
  border-right: 1px solid rgba(47, 59, 49, 0.719);

  li {
    font-size: 1.1rem;
    font-weight: bold;
    padding: 0.5rem;
    word-break: break-all;
  }
}
</style>
