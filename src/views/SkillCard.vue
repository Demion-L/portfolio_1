<template lang="">
  <div>
    <div class="box">
      <span></span>
      <div class="content">
        <h2>{{ title }}</h2>
        <ul>
          <li v-for="skill in skills" :key="skill">{{ skill }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    skills: Array,
  },
};
</script>

<style lang="scss" scoped>
.box {
  position: relative;
  width: 320px;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 40px 30px;
  transition: 0.5s;

  &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 50px;
    width: 50%;
    height: 100%;
    background: #fff;
    border-radius: 8px;
    transform: skewX(15deg);
    transition: 0.5s;
  }

  &::after {
    content: "";
    position: absolute;
    top: 0;
    left: 50px;
    width: 50%;
    height: 100%;
    background: #fff;
    border-radius: 8px;
    transform: skewX(15deg);
    transition: 0.5s;
    filter: blur(30px);
    transition: 0.5s;
  }

  &:hover::before,
  &:hover:after {
    transform: skewX(0deg);
    left: 20px;
    width: calc(100% - 90px);
  }

  &:nth-child(1)::before,
  &:nth-child(1)::after {
    background: linear-gradient(315deg, #2ac60e, #1985e4);
  }

  & span {
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 50;
    pointer-events: none;
  }

  & span::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border-radius: 8px;
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    opacity: 0;
    transition: 0.5s;
    animation: animate 2s ease-in-out infinite;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  }

  &:hover span::before {
    top: -50px;
    left: 50px;
    width: 100px;
    height: 100px;
    opacity: 1;
  }

  & span::after {
    content: "";
    position: absolute;
    bottom: 0;
    right: 0;
    width: 100%;
    height: 100%;
    border-radius: 8px;
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    opacity: 0;
    transition: 0.5s;
    animation: animate 2s ease-in-out infinite;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
    animation-delay: -1s;
  }

  &:hover span::after {
    bottom: -50px;
    right: 50px;
    width: 100px;
    height: 100px;
    opacity: 1;
  }

  &:hover .content {
    left: -25px;
  }
}

@keyframes animate {
  0%,
  100% {
    transform: translateY(10px);
  }
  50% {
    transform: translateY(-10px);
  }
}

.content {
  position: relative;
  left: 0;
  padding: 20px 40px;
  background: rgba(0, 0, 0, 0.05);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  backdrop-filter: blur(10px);
  z-index: 1;
  transition: 0.5s;
  color: #fff;

  h2 {
    font-size: 2em;
    color: #fff;
    margin-bottom: 10px;
  }

  p {
    font-size: 1.1em;
    margin-bottom: 10px;
    line-height: 1.4em;
  }

  ul {
    list-style-type: none;

    li {
      margin-bottom: 0.3rem;
    }
  }
}
</style>
