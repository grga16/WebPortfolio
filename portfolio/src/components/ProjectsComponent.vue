<template>
    <div class="projects">

        <div class="head-wrapper"><h1 id="projects">Projects</h1></div>

      <section class="projects-wrapper">

        <section class="row-one">
        <div class="project-one" v-for="(item, index) in items.slice(0, 3)" :key="index">
          <div @mouseover="disabled[index] = false" @mouseout="disabled[index] = true">
            <img :src="item.image" alt="">
            <p :class="{ disabled: disabled[index] }">{{ item.text }}</p>
          </div>
        </div>
      </section>

      <section class="row-one">
        <div class="project-one" v-for="(item, index) in items.slice(3, 6)" :key="index+3">
          <div @mouseover="disabled[index+3] = false" @mouseout="disabled[index+3] = true">
            <img :src="item.image" alt="">
            <p :class="{ disabled: disabled[index+3] }">{{ item.text }}</p>
          </div>
        </div>
      </section>
  
      </section>
    </div>
  </template>

<script>
export default {
    name: 'ProjectsComponent',
    data() {
        return {
            disabled: Array(6).fill(true),
            items: [
                {image: require('@/assets/minime.png'), text: 'This is my first project. It was a start of getting familliar with Adobe project workflow. The theme was mini-me.'},
                {image: require('@/assets/poster.png'), text: 'Poster for international day, one of the projects for improving skills in Adobe InDesign.'},
                {image: require('@/assets/beatup.png'), text: 'Beat up face, photoshop project for learning how to work with further styling and editing images.'},
                {image: require('@/assets/card.png'), text: 'Business card for showing important information about myself and my skillset on a simple card.'},
                {image: require('@/assets/cvimage.png'), text: 'My CV, a collection of information about my education so far, work experience and contact information in a simple, easily readable format.'},
                {image: require('@/assets/app.png'), text: 'One of the bigger projects, app for finding remote employment. Shows my growth as a software and UX designer'}
            ],
        };
    },
    // ...
};
</script>

<style scoped>
.head-wrapper{
    width: 80%;
    display: flex;
    justify-content: flex-start;
}

h1{
    color:  rgb(114, 166, 234);
    font-size: 3rem;
    font-weight: bold;
    display: flex;
    justify-content: flex-start;
    text-decoration: underline;
}
.projects{
    margin-top: 10%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.projects-wrapper{
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}
.row-one{
    width: 100vw;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly   ;
    flex-wrap: wrap;

}


.row-one div{
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
}

.project-one{
    position: relative;

    padding: 15px;
    background-color: rgb(23, 22, 22);
    border-radius: 10px;
    border: 1px #72a6ea solid;   
}

.project-one p{
    margin: 0;
    height: 92%;
    color: white;
    font-size: 1.2rem;
    font-weight: bold;
    background-color: rgba(33, 30, 30, 0.592);
    display: flex;
    justify-content: flex-end;
    flex-direction: column;
}


.row-one div p{
    width: 300px;
    z-index: 2;
    position: absolute;
}




img{
    width: 300px;
    height: 300px;
}

.disabled{
    visibility: hidden;
}
@media (max-width: 768px) {
  .projects-wrapper {
    flex-direction: column; /* Stack the project rows vertically */
  }

  .row-one{
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    flex-wrap: wrap;
  }

  .project-one {
    width: max-content; /* Make the project divs take up the full width */
    height: max-content;
    margin-bottom: 20px;
  }

  .project-one img {
    width: 100px; /* Make the images take up the full width of the project divs */
    height: auto; /* Maintain the images' aspect ratio */
  }

}

</style>