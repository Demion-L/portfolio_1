<template>
  <div class="container">
    <div class="about-me">
      <h1 data-text="About me">About me</h1>
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
        Recently, I completed a project using React.js, Typescript and Node.js
        for creating CLI to launch an interactive development environment for
        writing and documenting code.
        <br />
        <br />
        Previously, I worked as a Front-End Developer at WithSecure, where I
        contributed to developing a complex cyber security portal using Vue.js.
        Before that, I gained valuable experience as a Back-End Developer at
        SoftServe, working on a large real estate project using Node.js,
        TypeScript, and PostgreSQL.
        <br />
        <br />
        I'm a strong team player with excellent communication and collaboration
        skills. I'm eager to find a team where I can continue learning,
        contribute to meaningful projects, and have fun collaborating with
        colleagues.
      </p>
    </div>
    <div class="cards-container">
      <skill-card
        v-for="skillset in skills"
        :key="skillset.type"
        :title="skillset.type"
        :skills="skillset.items"
      />
    </div>

    <div class="button-container">
      <!-- <div class="projects-btn">
        <a href="">My projects</a>
      </div> -->
      <link-button :link="link" :content="content" />
    </div>
  </div>
</template>

<script>
import SkillCard from "@/views/SkillCard.vue";
import LinkButton from "@/views/LinkButton.vue";

export default {
  components: {
    SkillCard,
    LinkButton,
  },

  data() {
    return {
      skills: [
        {
          type: "Frontend",
          items: ["Vue.js", "Vuex", "React", "Redux", "Typescript", "MUI"],
        },
        {
          type: "Backend",
          items: ["Node.js", "Express"],
        },
        {
          type: "Databases",
          items: ["MySQL", "MongoDB", "PostsgreSQL"],
        },
        {
          type: "Unit testing",
          items: ["Jest", "Mocha", "Chai"],
        },
        {
          type: "Soft Skills",
          items: ["Communication", "Teamwork", "Problem-solving"],
        },
      ],
      link: "https://drive.google.com/file/d/1i5OnCmcvHXyJRTWWLrWjcT-gXcdnOE42/view?usp=sharing",
      content: "My CV",
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  border: 1px solid #fff;
  background-color: rgba(8, 85, 106, 0.83);
  width: 70%;
  display: flex;
  flex-direction: column;
  margin: 0.5rem;
  color: rgb(208, 209, 232);
  border-radius: 4px;
  font-size: 1.1rem;
}

.cards-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

h1 {
  margin-bottom: 1rem;
  font-family: "Poppins", sans-serif;
  font-size: 2rem;
}
.about-me {
  padding: 1rem;

  &__info {
    text-align: left;
    font-size: 1.1em;
    letter-spacing: 1.4px;
    line-height: 1.2;
    padding: 0.5rem;
    border-top: 1px solid rgb(245, 245, 240);
    border-left: 1px solid rgb(245, 245, 240);
    border-bottom: 1px solid rgba(18, 19, 18, 0.538);
    border-right: 1px solid rgba(18, 19, 18, 0.538);
    border-radius: 5px;
    backdrop-filter: blur(3px);
  }
}
</style>
