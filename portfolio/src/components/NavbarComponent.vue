<template>
    <nav class="nav">
        <div class="nav-wrapper">
            <div class="nav-wrapper-content"><img src="../assets/logo.png" class="brand-logo">
            <ul id="nav-mobile" class="right hide-on-med-and-down">
                <li><a href="#">Home</a></li>
                <li><a href="#about">About Me</a></li>
                <li><a href="#cv">CV</a></li>
                <li><a href="#projects">Projects</a></li>
            </ul></div>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'NavbarComponent',
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

@keyframes linkHoverGrow {
  0% {
    transform: scale(1);
  }
  100% {
    transform: scale(1.2);
  }
}
    .nav{
        position: fixed;
        z-index: 5;
    }
    .nav-wrapper {
        width: 100vw;
        height: max-content;
        background-color: #000000;
        display: flex;
        justify-content: flex-start; 
        align-items: center;
        flex-direction: row;
       
    }

    .nav-wrapper-content {
        width: 80%;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        flex-direction: row;
    }
    .hide-on-med-and-down {
        width: 50%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-direction: row;
    }

    li {
        list-style-type: none;
    }
    
    a {
        color: rgb(114, 166, 234);
        font-weight: bold;
        text-decoration: none;
    }

    a:hover {
        color: rgb(255, 255, 255);
        animation:  0.5s ease-in-out;
    }

    .brand-logo{
        width: 50px;
        height: 50px;
    }

    @media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    align-items: center;
  }

  .navbar .nav-item {
    margin: 10px 0; 
    padding: 10px;
    text-align: center; 
  }

  a{
    font-size: 8px;
  }

  .brand-logo{
    height: 20px;
    width: 20px;
  }

  #nav-mobile{
    padding: 0;
  }

  .nav-wrapper-content{
    width: 60%;
  }

  
}
</style>