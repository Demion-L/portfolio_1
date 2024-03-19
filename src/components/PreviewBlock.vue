<template>
  <div class="container">
    <img class="my-photo" src="../assets/my photo/3.jpg" alt="my photo" />
    <div class="profile">
      <h1 class="profile-name">Dmytro Latysh</h1>
      <p class="profile-occupation">Full-Stack Developer</p>
    </div>
    <social-links />
    <my-contacts />
  </div>
</template>

<script>
import SocialLinks from "../views/SocialLinks.vue";
import MyContacts from "../views/MyContacts.vue";
export default {
  components: {
    SocialLinks,
    MyContacts,
  },
};
</script>

<style lang="scss" scoped>
.container {
  background: rgba(229, 34, 34, 0.467),
    url("../assets/main\ bg/coding-neon.jpg");
  width: 30%;
  display: flex;
  flex-direction: column;
}

.my-photo {
  width: 100%;
  margin-bottom: 2rem;
  border-bottom: 2px solid rgba(31, 31, 25, 0.296);
  border-right: 2px solid rgba(255, 251, 5, 0.584);
  border-radius: 0 0 5px 0;
}

.profile {
  color: white;
  border-top: 1px solid rgb(245, 245, 240);
  border-left: 1px solid rgb(245, 245, 240);
  border-bottom: 1px solid rgba(47, 59, 49, 0.782);
  border-right: 1px solid rgba(47, 59, 49, 0.719);
  border-radius: 5px;
  backdrop-filter: blur(5px);
  margin: 1rem 2rem;

  p {
    padding: 0.5rem;
  }
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (min-width: 600px) {
}
/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (max-width: 600px) {
}
/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (max-width: 768px) {
  .container {
    margin-bottom: 1rem;
    padding: 1rem 2rem;
    width: 100%;
    border: 1px solid rgb(218, 212, 212);
  }

  .my-photo {
    border-radius: 50%;
  }
}
</style>
