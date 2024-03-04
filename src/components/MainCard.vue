<template lang="">
  <div class="main-container">
    <div class="container-one">
      <img class="my-photo" src="../assets/my photo/3.jpg" alt="my photo" />
      <div class="profile">
        <h1 class="profile-name">Dmytro Latysh</h1>
        <p class="profile-occupation">Software Developer</p>
      </div>
      <div class="social-links">
        <ul>
          <li>
            <a href="">
              <img
                src="../assets/social media/github-94.png"
                alt="github logo"
              />
              <span>Github</span>
            </a>
          </li>
          <li>
            <a href="">
              <img
                src="../assets/social media/linkedin-logo-64.png"
                alt="linkedin logo"
              />
              <span>Linkedin</span>
            </a>
          </li>
          <li>
            <a href="">
              <img
                src="../assets/social media/facebook-circled-64.png"
                alt="fb logo"
              />
              <span>Facebook</span>
            </a>
          </li>
        </ul>
      </div>
    </div>

    <div class="container-two">
      <div class="about-me">
        <h1>About me</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium
          id perferendis dolorum impedit deserunt dicta voluptatum odit veniam
          minima. Est beatae voluptate maxime? Qui nihil quas quo, esse
          accusamus debitis.
        </p>
      </div>
      <div class="tech-section">
        <h2>Technologies Studied</h2>
        <ul>
          <li>
            Frontend
            <ul>
              <li>JavaScript</li>
              <li>TypeScript</li>
              <li>Vue.js</li>
              <li>Vuex</li>
              <li>React.js</li>
              <li>Redax</li>
            </ul>
          </li>
          <li>
            Backend
            <ul>
              <li>Node.js</li>
              <li>Express.js</li>
            </ul>
          </li>
          <li>
            Database
            <ul>
              <li>PostgreSQL</li>
              <li>MySQL</li>
              <li>MongoDB</li>
            </ul>
          </li>
          <li>
            Unit testing
            <ul>
              <li>Jest</li>
            </ul>
          </li>
        </ul>
      </div>

      <div class="button-container">
        <div class="projects-btn">
          <a href="">My projects</a>
        </div>
        <div>
          <a href="">My Resume</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
img {
  width: 30px;
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
}

.container {
  &-one {
    background-color: rgba(240, 244, 186, 0.759);
    width: 30%;
    display: flex;
    flex-direction: column;
  }

  &-two {
    background-color: rgba(189, 236, 249, 0.84);
    width: 70%;
    display: flex;
    flex-direction: column;
  }
}

.social-links {
  padding: 1.5%;

  ul {
    width: 80%;
    border: 1px solid rgb(236, 62, 62);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    background-color: rgba(202, 209, 67, 0.593);
    border-radius: 5px;
    border: 1px solid rgba(255, 255, 255, 0.125);
  }

  li {
    padding: 1% 2.5%;

    a {
      color: rgb(23, 24, 15);
      display: flex;
      align-items: center;
    }
  }
}
</style>
