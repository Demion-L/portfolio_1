<template lang="">
  <div class="social-links">
    <ul>
      <li>
        <a href="https://github.com/Demion-L" data-replace="Github">
          <img src="../assets/social media/github-94.png" alt="github logo" />
          <span>Github</span>
        </a>
      </li>
      <li>
        <a
          href="https://www.linkedin.com/in/dmitriy-latysh/"
          data-replace="Linkedin"
        >
          <img
            src="../assets/social media/linkedin-logo-64.png"
            alt="linkedin logo"
          />
          <span>Linkedin</span>
        </a>
      </li>
      <li>
        <a
          href="https://www.facebook.com/profile.php?id=100087912827059"
          data-replace="Facebook"
        >
          <img
            src="../assets/social media/facebook-circled-64.png"
            alt="fb logo"
          />
          <span>Facebook</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
img {
  width: 3rem;
}

.social-links {
  padding: 1.5%;
  margin: 0 1.4rem;

  ul {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
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
  }

  li {
    padding: 1% 2.5%;

    a {
      color: rgb(23, 24, 15);
      display: flex;
      padding: 0 1rem;
      font-weight: bold;
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
</style>
