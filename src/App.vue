<template>
  <div id="back">
    <div id="app">
      <TheNavbar></TheNavbar>
      <div style="max-width: 900px; margin:auto;" class="is-centered">
        <AboutMe id="about"></AboutMe>
        <Project id="projects" image="agami_landing.svg" title="Agami">
          <template v-slot:text>
            <p>This is a test</p>
          </template>
        </Project>
        <MoreInformation id="more"></MoreInformation>
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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
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
</style>
