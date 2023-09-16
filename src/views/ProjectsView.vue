<script setup>
import { Carousel, Navigation, Slide } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'

const slides = [
  {
    id: 1,
    title: 'Project HRNet',
    content: '/website/src/assets/hrnet.png'
  },
  {
    id: 2,
    title: 'Date Picker',
    content: '/website/src/assets/datepicker.png'
  },
  {
    id: 3,
    title: 'Table',
    content: '/website/src/assets/table.png'
  },
]
</script>

<template>
  <div class="Projects">
    <div class="Project"> 
      <h2>Project HRNet</h2>
      <Carousel>
        <Slide v-for="slide in slides" :key="slide.id">
          <div class="carousel__item">
            <a :href="slide.content" target="_blank">
              <img class="project_img" :src="slide.content" :alt="slide.title" />
            </a>
          </div>
        </Slide>
        <template #addons>
          <Navigation />
          <Pagination />
        </template>
      </Carousel>
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
      <a href="src/assets/Sportsee.png" target="_blank">
        <img class="project_img" src="../assets/Sportsee.png" alt="Sportsee" />
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
    border-radius: 20px;
    margin-top: 1rem
}
.little-icon{
  width: 50px;
  height: 50px;
  margin: 0 1rem;
}
</style>
