<template>
    <div class="projects">
        <section class="projects-wrapper">
            <section class="row-one">
                <div class="project-one" @mouseover="toggleDescription(true)" @mouseout="toggleDescription(false)">
                    <img src="../assets/about.jpg" alt="">
                    <div :class="{ disabled: disabled }">Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur omnis quis iusto at error facere culpa praesentium cumque odio voluptate reprehenderit consectetur recusandae sunt harum, excepturi voluptatum consequuntur dolorem eius.</div>
                </div>
                <div class="project-one" @mouseover="toggleDescription(true)" @mouseout="toggleDescription(false)">
                    <img src="../assets/about.jpg" alt="">
                    <div :class="{ disabled: disabled }">Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur omnis quis iusto at error facere culpa praesentium cumque odio voluptate reprehenderit consectetur recusandae sunt harum, excepturi voluptatum consequuntur dolorem eius.</div>
                </div>
                <div class="project-one" @mouseover="toggleDescription(true)" @mouseout="toggleDescription(false)">
                    <img src="../assets/about.jpg" alt="">
                    <div :class="{ disabled: disabled }">Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur omnis quis iusto at error facere culpa praesentium cumque odio voluptate reprehenderit consectetur recusandae sunt harum, excepturi voluptatum consequuntur dolorem eius.</div>
                </div>
            </section>

            <section class="row-one">
                <div class="project-one" @mouseover="toggleDescription(true)" @mouseout="toggleDescription(false)">
                    <img src="../assets/about.jpg" alt="">
                    <div :class="{ disabled: disabled }">Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur omnis quis iusto at error facere culpa praesentium cumque odio voluptate reprehenderit consectetur recusandae sunt harum, excepturi voluptatum consequuntur dolorem eius.</div>
                </div>
                <div class="project-one" @mouseover="toggleDescription(true)" @mouseout="toggleDescription(false)">
                    <img src="../assets/about.jpg" alt="">
                    <div :class="{ disabled: disabled }">Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur omnis quis iusto at error facere culpa praesentium cumque odio voluptate reprehenderit consectetur recusandae sunt harum, excepturi voluptatum consequuntur dolorem eius.</div>
                </div>
                <div class="project-one" @mouseover="toggleDescription(true)" @mouseout="toggleDescription(false)">
                    <img src="../assets/about.jpg" alt="">
                    <div :class="{ disabled: disabled }">Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur omnis quis iusto at error facere culpa praesentium cumque odio voluptate reprehenderit consectetur recusandae sunt harum, excepturi voluptatum consequuntur dolorem eius.</div>
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
            disabled: false // Initialize disabled as false
        };
    },
    methods: {
        toggleDescription(status) {
            this.disabled = status;
        }
    }
};
</script>

<style scoped>
.projects{
    margin-top: 10%;
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
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;

}


.row-one div{
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
}



.row-one div div{
    width: 300px;
    position: absolute;
    z-index: 2;
}




img{
    width: 300px;
    height: 300px;
}

.disabled{
    display: none;
}
</style>