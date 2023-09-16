<template>
  <div class="front"> 
      <div class="presentation">
          <div class="blurb">
              Passionnée d'informatique depuis l'enfance et curieux de nature, j'ai choisi de me reconvertir dans le développement afin pouvoir joindre ma passion et ma carrière professionnelle.
          </div>
          <div class="title">
              <h1>Alex GROUARD</h1>
              <h2>Developpeur Web</h2>
          </div>
      </div> 
      <div class="icon">
          <a href="https://www.linkedin.com/in/alex-grouard-a3109b19/" target="_blank">
              <img src="src/assets/linkedin.png" alt="linkedin" />
          </a>
          <a href="https://github.com/AlexGrouard" target="_blank">
              <img src="src/assets/github.png"  alt="github" />
          </a>
          <a href="mailto:alex.m.grouard@gmail.com" target="_blank">
              <img src="src/assets/email.svg" alt="email" />
          </a>
      </div>
  </div> 
</template>

<style scoped>
.front {
  margin: 35vh 5vh;
}
.presentation {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.blurb {
  width: 50%;
  font-size: 1.5rem;
  text-align: justify;
}
.title {
  width: 50%;
  text-align: right;
}
.icon {
  display: flex;
  align-items: center;
  margin-top: 1vh;
}
.icon img {
  width: 3vh;
  margin-right: 2vh;
}

</style>
