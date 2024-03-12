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
        Recently, I completed a project using Next.js to build an application
        for.
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
      <div class="projects-btn">
        <a href="">My projects</a>
      </div>
      <div>
        <a href="">My Resume</a>
      </div>
    </div>
  </div>
</template>

<script>
import SkillCard from "../views/SkillCard.vue";

export default {
  components: {
    SkillCard,
  },

  data() {
    return {
      skills: [
        { type: "Frontend", items: ["Vue.js", "React", "HTML", "CSS"] },
        {
          type: "Backend",
          items: ["Node.js", "Express", "Databases"],
        },
        {
          type: "Soft Skills",
          items: ["Communication", "Teamwork", "Problem-solving"],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  border: 1px solid #fff;
  background-color: rgba(116, 214, 241, 0.83);
  width: 70%;
  display: flex;
  flex-direction: column;
  margin: 0.5rem;
  color: rgb(4, 9, 102);
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
  position: relative;
  font-family: "Poppins", sans-serif;
  font-size: 2rem;

  &:hover::before {
    content: attr(data-text);
    position: absolute;
    top: 0;
    left: 0;
    color: #313f97;
  }
  &:hover::after {
    content: attr(data-text);
    position: absolute;
    color: transparent;
    top: 110px;
    left: 10px;
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-stroke: 1px #ec2225;
  }
}
.about-me {
  padding: 1rem;
  position: relative;

  &__info {
    text-align: left;
  }
}
</style>
