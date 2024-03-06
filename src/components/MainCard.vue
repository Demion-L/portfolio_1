<template lang="">
  <div class="main-container"></div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
img {
  width: 2rem;
}

ul,
li {
  list-style-type: none;
}

a {
  text-decoration: none;
}

.my-photo {
  width: 100%;
}

.main-container {
  display: flex;
  background: url("../assets/main\ bg/code.jpg");
}

.container {
  &-one {
    background: rgba(229, 34, 34, 0.467),
      url("../assets/main\ bg/coding-neon.jpg");
    width: 30%;
    display: flex;
    flex-direction: column;
  }

  &-two {
    background-color: rgba(116, 214, 241, 0.83);
    width: 70%;
    display: flex;
    flex-direction: column;
    margin: 0.5rem;
    color: rgb(1, 13, 19);
    border-radius: 4px;
  }
}

.profile {
  color: white;
}

.social-links {
  padding: 1.5%;

  ul {
    width: 80%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    background-color: rgba(245, 245, 7, 0.871);
    border-radius: 5px;
    border-top: 3px solid rgb(245, 245, 240);
    border-left: 3px solid rgb(245, 245, 240);
    border-bottom: 3px solid rgba(47, 59, 49, 0.404);
    border-right: 3px solid rgba(47, 59, 49, 0.404);
  }

  li {
    padding: 1% 2.5%;

    a {
      color: rgb(23, 24, 15);
      display: flex;
      padding: 0 1rem;
      align-items: center;
      position: relative;
      border: 2px solid rgba(255, 255, 255, 0);
      border-radius: 4px;

      &:hover {
        border-top: 2px solid rgb(245, 245, 240);
        border-left: 2px solid rgb(245, 245, 240);
        border-bottom: 2px solid rgba(47, 59, 49, 0.404);
        border-right: 2px solid rgba(47, 59, 49, 0.404);
      }
      &:active {
        border-top: 2px solid rgba(47, 59, 49, 0.404);
        border-left: 2px solid rgba(47, 59, 49, 0.404);
        border-bottom: 2px solid rgb(245, 245, 240);
        border-right: 2px solid rgb(245, 245, 240);
      }
    }
  }
}

.about-me {
  padding: 1rem;

  &__info {
    text-align: left;
  }
}
</style>
