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
            <a href="" data-replace="Github">
              <img
                src="../assets/social media/github-94.png"
                alt="github logo"
              />
              <span>Github</span>
            </a>
          </li>
          <li>
            <a href="" data-replace="Linkedin">
              <img
                src="../assets/social media/linkedin-logo-64.png"
                alt="linkedin logo"
              />
              <span>Linkedin</span>
            </a>
          </li>
          <li>
            <a href="" data-replace="Facebook">
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
        <p class="about-me__info">
          Enthusiastic Full-Stack Developer. I'm a passionate developer with 2+
          years of experience building web applications.
          <br />
          <br />
          I'm currently expanding my skillset by learning advanced web UI
          technologies. I'm particularly excited about the challenge of creating
          user-friendly and visually appealing interfaces.
          <br />
          <br />
          Recently, I completed a project using [mention specific technologies]
          to build a [brief description of the project].
          <br />
          <br />
          Previously, I worked as a Front-End Developer at WithSecure, where I
          contributed to developing a complex cyber security portal using
          Vue.js. Before that, I gained valuable experience as a Full-Stack
          Developer at SoftServe, working on a large real estate project using
          Node.js, TypeScript, and PostgreSQL.
          <br />
          <br />
          I'm a strong team player with excellent communication and
          collaboration skills. I'm eager to find a team where I can continue
          learning, contribute to meaningful projects, and have fun
          collaborating with colleagues.
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
    background-color: rgba(189, 236, 249, 0.84);
    width: 70%;
    display: flex;
    flex-direction: column;
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
    width: 55%;

    a {
      color: rgb(23, 24, 15);
      display: flex;
      align-items: center;
      overflow: hidden;
      position: relative;

      &::before,
      &::after {
        content: "";
        position: absolute;
        width: 100%;
        left: 0;
      }
      &::before {
        background-color: #1b2bbb;
        height: 2px;
        bottom: 0;
        transform-origin: 100% 50%;
        transform: scaleX(0);
        transition: transform 0.3s cubic-bezier(0.76, 0, 0.24, 1);
      }
      &::after {
        content: attr(data-replace);
        height: 100%;
        top: 15%;
        left: 10%;
        transform-origin: 100% 50%;
        transform: translate3d(200%, 0, 0);
        transition: transform 0.3s cubic-bezier(0.76, 0, 0.24, 1);
        color: #1b2bbb;
        font-weight: bold;
      }

      &:hover::before {
        transform-origin: 0% 50%;
        transform: scaleX(1);
      }
      &:hover::after {
        transform: translate3d(0, 0, 0);
      }

      & span {
        display: inline-block;
        transition: transform 0.3s cubic-bezier(0.76, 0, 0.24, 1);
      }

      &:hover span {
        transform: translate3d(-200%, 0, 0);
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
