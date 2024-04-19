<template>
  <div id="app">
    <NavbarComponent />
    <section class="text-wrapper">
      <h1 class="welcome-text">Welcome to my portfolio</h1>
    </section>
    <AboutComponent />
    <CvComponent />
    <ProjectsComponent/>
    <FooterComponent />
  </div>
</template>

<script>
import NavbarComponent from './components/NavbarComponent.vue'
import AboutComponent from './components/AboutComponent.vue';
import CvComponent from './components/CvComponent.vue'
import ProjectsComponent from './components/ProjectsComponent.vue';
import FooterComponent from './components/FooterComponent.vue';

export default {
  name: 'App',
  components: {
    NavbarComponent,
    AboutComponent,
    CvComponent,
    ProjectsComponent,
    FooterComponent
  }
}
</script>

<style>
@keyframes fade-in{
  0%{
    opacity: 0;
  }
  100%{
    opacity: 100;
  }
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
  height: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: column;
  
}

body {
  margin: 0;
  width: 100vw;
  background-color: #0e0e0e;
  overflow-x: hidden;
}

.welcome-text{
  font-weight: bold;
  font-size: 4rem;
  color: rgb(114, 166, 234);
  animation: fade-in 3s forwards ;
  margin-top: 40%;
  text-decoration: underline;
}

@media (max-width: 768px) {
  body{
    overflow-x: hidden;
  }

  .welcome-text{
    font-size: 1.1rem;
    max-width: 50%;
  }
  
}
</style>
