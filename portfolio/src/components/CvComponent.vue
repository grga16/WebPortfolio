<template>
    <div class="video" id="cv">
        <section class="video-wrapper">
            <div class="video-description"><h1 class="video-head">Video CV</h1>
            <div class="video-text">This is my video CV, a good way to get to know me a little it better in under 2 minutes</div></div>
            <iframe class="iframe" src="https://www.youtube.com/embed/5aFo4PKm0G0" frameborder="0"></iframe>
            
        </section>
        <div class="pdf-wrapper"><a href="https://drive.google.com/file/d/1xyEbHc7TmJQ3PSZSdOw474hO_iWa4nnv/view?usp=sharing" class="pdf-button" target="_blank">Download PDF</a></div>
    </div>
</template>

<script>
export default {
    name: 'CvComponent',
    data() {
        return {
        };
    },
    methods: {
    },
    computed: {
    },
};
</script>

<style scoped>
.video{
    margin-top: 10%;
    height: 100%;
}
.video-wrapper{
    height: auto;
    width: 100vw;
    height: max-content;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    flex-direction: row;
}

.video-description{
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;

}

.video-text{
    padding: 10px;
    text-align: center;
    max-width: 300px;
    font-size: 1.1rem;
    color: #ffffff;
    background-color: rgb(23, 22, 22);
    border-radius: 10px;
    border: 1px rgb(114, 166, 234) solid;
}

.video-head{
    color:  rgb(114, 166, 234);
    font-size: 3rem;
    font-weight: bold;
    text-decoration: underline;
    margin-bottom: 50%;
    margin-top: 0;
}

.iframe{
    width: 470px;
    height: 365px;
}

.pdf-wrapper{
    margin-top: 5%;
    width: 100%;
    display: flex;
    justify-content: center;
}

.pdf-button{
    background-color: rgb(114, 166, 234);
    border-radius: 5px;
    border: black;
    width: 200px;
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    color: white;
}

@media (max-width: 768px) {
  .video-wrapper {
    flex-direction: column; 
    align-items: center; 
  }

  .iframe {
    width: 90%; 
    height: auto; 
    margin-top: 20px;
  }

  .pdf-wrapper {
    text-align: center; 
  }

  .video-head{
    margin: 5%;
  }
}
</style>