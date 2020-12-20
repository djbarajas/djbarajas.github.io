<template>
  <div id="back">
    <div id="app">
      <TheNavbar></TheNavbar>
      <div style="max-width: 900px; margin:auto;" class="is-centered py-5">
        <AboutMe id="about"></AboutMe>
        <h1 id="projects" class="mt-6 has-text-grey-lighter title is-2">Projects</h1>
        <Project image="agami_landing.svg" title="Agami">
          <template v-slot:text>
            <p>
              Designed a weather predictor using machine learning
              XGBoost given location based on the date, time, and location
              to visualize streaming data. Training and testing models
              through Scikit-Learn in order to increase efficiency and speed.
              Extended applications for the algorithm can be used for any data.
            </p>
            <div class="columns is-vcentered is-centered">
              <div class="column">
                <b><a href="https://ewwong2.github.io/Agami/">Website</a></b>
              </div>
              <div class="column">
                <b><a href="https://www.cs.usfca.edu/~apjoshi/papers/agami-bdcat2020.pdf">Research Paper</a></b>
              </div>
            </div>
          </template>
        </Project>
        <Project image="canvas-by-instructure-logo.png" title="Rubrics From Canvas">
          <template v-slot:text>
            <p>
              Analyzed feedback from students reviews in a Data Visualization class using
              python sentiment detection libraries and MySQL, VADER. The code to gather
              Canvas Course data can be found below.
            </p>
            <div class="my-2">
            <b><a href="https://github.com/djbarajas/canvas-rubrics-api">Code</a></b>
            </div>
          </template>
        </Project>
        <Project image="Yelp_Logo.svg" title="Restaurant Recommender">
          <template v-slot:text>
            <p>
              Created a restaurant recommender using Pearson's Correlation along with
              a page computing the tf-idf of a set of reviews of a restaurant to find
              frequent topics.  Data was gathered through the Yelp API of restaurants
              in San Francisco and stored in an in memory database using Sqlite3.
            </p>
          </template>
        </Project>
        <h1 id="more" class="mt-6 has-text-grey-lighter title is-2">More Information</h1>
        <MoreInformation></MoreInformation>
      </div>
    </div>
  </div>
</template>

<script>
import TheNavbar from '@/components/TheNavbar.vue';
import AboutMe from '@/components/AboutMe.vue';
import Project from '@/components/Project.vue';
import MoreInformation from '@/components/MoreInformation.vue';

export default {
  name: 'App',
  components: {
    MoreInformation,
    Project,
    AboutMe,
    TheNavbar,
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans&family=Raleway&display=swap');

#app {
  font-family: Raleway, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#back {
  background: linear-gradient(217deg, rgba(44,79,153,.8), rgba(255,0,0,0) 70.71%),
  linear-gradient(127deg, rgba(44,124,153,.8), rgba(0,255,0,0) 70.71%),
  linear-gradient(336deg, rgba(72,77,161,.8), rgba(0,0,255,0) 70.71%);
}
h1, h2, h3, h4, h5, h6 {
  font-family: 'Open Sans', Raleway, Avenir, Helvetica, Arial, sans-serif;
}
</style>
