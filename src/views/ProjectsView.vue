<script setup>
import { useCycleList } from '@vueuse/core'
const { state, prev, next } = useCycleList([
  '/src/assets/project/hrnet.png',
 '/src/assets/project/datepicker.png',
 '/src/assets/project/table.png'
]);
</script>

<template>
  <div class="Projects">
    <div class="Project"> 
      <h2>Project HRNet</h2>
      <div class="carousel">
          <img src='../assets/left.png' @click="prev()" alt="left" class="leftArrow"/>
            <a :href="state" target="_blank">
              <img class="project_img" :src="state" alt="hrnet"/>
            </a>
          <img src="../assets/right.png" @click="next()" alt="right" class="rightArrow"/>
      </div>
      <p class="blurb">The goal of this project was to recreate an existing Jquery page in React.<br />
        For this I've selected a few components to implement and develop the date picker from scratch.<br />
        it's available here: <a href="https://www.npmjs.com/package/date-picker-typescript">date-picker-typescript </a>
      </p>
      <div class="icons">
        <img class="little-icon" src="../assets/skills/Typescript.svg">
        <img class="little-icon" src="../assets/skills/React.svg">
        <img class="little-icon" src="../assets/skills/Sass.svg">
      </div>
    </div>
    <div class="Project"> 
      <h2>Project Sportsee</h2>
      <a href="/assets/Sportsee.png" target="_blank">
        <img class="project_img" src="../assets/project/Sportsee.png" alt="Sportsee" />
      </a>
      <p class="blurb">The goal of this project was to create a dashboard connect to an existing API.<br />
        For this I've used React and Recharts.js for all the charts.<br />
      </p>
      <div class="icons">
        <img class="little-icon" src="../assets/skills/Typescript.svg">
        <img class="little-icon" src="../assets/skills/React.svg">
        <img class="little-icon" src="../assets/skills/Sass.svg">
      </div>
    </div>
  </div>
</template>

<style scoped>
.Projects {
    display: flex;
    justify-content: center;
    flex-wrap: wrap ;
}
.Project{
 width: calc(50% - 2rem);
 margin-right: 2rem;
 margin-top: 10%;
}
.project_img {
    width: 100%;
    height: 450px;
    object-fit: contain;
    margin-top: 1rem
}
.little-icon{
  width: 50px;
  height: 50px;
  margin: 0 1rem;
}
.carousel{
  display: flex;
  justify-content: center;
  align-items: center;
}

.leftArrow{
  margin-right: 1rem;
}
.rightArrow{
  margin-left: 1rem;
}
</style>
