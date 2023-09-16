<template>
  <div class="skills">
    <div class="skill">
      <img src="../assets/skills/JavaScript.svg" alt="JS" />
      <h3>Javascript</h3>
    </div>
    <div class="skill">
      <img src="../assets/skills/Typescript.svg" alt="TS" />
      <h3>Typescript</h3>
    </div>
    <div class="skill">
      <img src="../assets/skills/React.svg" alt="React" />
      <h3>React</h3>
    </div>
    <div class="skill">
      <img src="../assets/skills/logoVue.svg" alt="Vue" />
      <h3>Vue</h3>
    </div>
    <div class="skill">
      <img src="../assets/skills/HTML5.svg" alt="html" />
      <h3>HTML</h3>
    </div>
    <div class="skill">
      <img src="../assets/skills/CSS3.svg" alt="CSS" />
      <h3>CSS</h3>
    </div>
    <div class="skill">
      <img src="../assets/skills/Sass.svg" alt="SASS" />
      <h3>SASS</h3>
    </div>

  </div>
</template>

<style scoped>
.skills {
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
}
.skill {
    margin: 5rem 2rem;
    width: calc(25%);
    height: 200px;
}
.skill img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    border-radius: 20px;
}

h3 {
    text-align: center;
    font-size: 2rem;
}
@media screen and (max-width: 1024px) {

  .skill {
    margin: 2rem 0;
    width: calc(30%);
    height: 120px;
  }
  h3 {
    font-size: 1.5rem;
    margin: auto 0;
  }
}
</style>
