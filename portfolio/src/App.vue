<template>
  <div id="app">
    <NavbarComponent />
    <section>
      <h1 class="welcome-text">Welcome to my portfolio</h1>
    </section>
    <AboutComponent />
    <router-view />
  </div>
</template>

<script>
import NavbarComponent from './components/NavbarComponent.vue'
import AboutComponent from './components/AboutComponent.vue';

export default {
  name: 'App',
  components: {
    NavbarComponent,
    AboutComponent
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
  width: 100vw;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: column;
  
}

body {
  margin: 0;
  width: 100vw;
  background-color: rgb(14, 14, 14);
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
</style>
