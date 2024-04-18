<template>
    <div class="about-wrapper">
        <h1 class="about-head">About Me</h1>
        <section class="about">
            <img class="about-img" src="../assets/about.jpg" alt="">
            <div class="about-text">Hello my name is Grgur Ivic and I am student at EASV. I was born in Zagreb, Croatia and I moved to denmark to study multimedia design. Since high schools I was interested in that area and that is why I decided to continue my education in that direction. I am a creative and adventurous person. I love to travel a lot and meet new people and see different cultures. I’m also a big fan of sports and I have been playing football since I was 7 years old. Throughout my education I want to improve my skills in programming but also in designing. My goal is to improve my skills and become a multimedia designer after my studies. I need to start from somewhere so this portfolio is a small beginning of my journey. Here you can find my video CV as well as some of my projects.</div>
        </section>
    </div>
</template>

<script>
export default {
    name: 'AboutComponent',
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
.about-wrapper{
    margin-top: 20%;
    width: 100%;
    height: max-content;
    display: flex;
    align-items: center;
    flex-direction: column;
}
.about{
    width: 80%;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
}

.about-img{
    width: 250px;
    height: 400px;
}

.about-text{
    padding: 20px;
    text-align: center;
    max-width: 400px;
    font-size: 1.1rem;
    color: #ffffff;
    background-color: rgb(23, 22, 22);
    border-radius: 10px;
    border: 1px rgb(114, 166, 234) solid;
}

.about-head{
    color:  rgb(114, 166, 234);
    width: 58%;
    font-size: 3rem;
    font-weight: bold;
    display: flex;
    justify-content: flex-start;
    text-decoration: underline;
}

</style>