<template>
    <div class="footer">

        <div class="info">

            <div class="image-wrapper">
                <img src="../assets/logo.png" alt="logo">
            </div>

            <div class="contact">
                <p>
                    You can contact me on my email:
                </p>
                <p>
                    grgurskreblin@gmail.com 
                </p>
            </div>

            <div class="icons">
                <a href="https://www.linkedin.com/in/grgur-ivi%C4%87-ba751b278/"><img src="../assets/linkedin.svg" alt="L" class="linkedin"></a>
                <a href="https://www.facebook.com/grgur.ivic"><img src="../assets/facebook.svg" alt="F" class="facebook"></a>
                <a href="https://www.instagram.com/_grgurivic_?igsh=MW1yZWZ4azFqcGpkbg=="><img src="../assets/instagram.svg" alt="I" class="instagram"></a>
                
                
                

            </div>

        </div>
        
        <div class="copyright">
            <p>Ⓒ 2024 All rights reserved</p>
        </div>

    </div>

</template>

<script>
export default {
    name: 'FooterComponent',
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
p{
    color: white;
}

img{
    width: 50px;
    height: 50px;
}

.footer{
    margin-top: 20%;
    background-color: black;
    width: 100vw;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

.info{
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 60%;
}

.icons{
    display: flex;
    justify-content: space-between;
    align-items: center;

}

.linkedin{
    width: 40px;
    height: 40px;
}
.instagram{
    width: 50px;
    height: 50px;
}

.facebook{
    width: 70px;
    height: 70px;
}

@media (max-width: 768px) {
  .footer {
    flex-direction: column; /* Stack the footer items vertically */
    align-items: center; /* Center the footer items horizontally */
    margin-top: 250px;
  }

  .info{
    justify-content: space-between;
    align-items: center;
    width: 100%;
}

  .footer-item {
    margin: 10px 0; /* Add some vertical margin between footer items */
  }

  img{
    width: 30px;
    height: 30px;
}

p{
    font-size: 0.5rem;
}
}
</style>