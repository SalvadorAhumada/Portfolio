<template>
    <div class="about-me">
        <div class="return">
          <span  @click="$emit('close-modal')" class="material-icons">
            arrow_upward
          </span>
        <h2>Hello there !</h2>
        <div class="about-me-text">
            <p> My name is Salvador and I'm a self-taught developer.</p>
            <p>I started watching Youtube tutorials and Udemy courses. Eventually I was able to create a <a href="https://github.com/salvadorAhumada" target="_blank">github repository</a> that caught the interest of the right people and gave me my first job in the industry.</p>
            <p>I'm always learning new things. What started as a career in frontend has slowly been turn into a career in fullstack developer</p>
            <p>Current stack: Vue, Express, Postgress. Transitioning to MERN stack</p>
        </div>
        </div>
    </div>
</template>

<script>
export default {
 methods:{
 }   
}
</script>

<style scoped>
    .about-me {
        position:fixed;
        left:0;
        right:0;
        top:0;
        bottom:0;
        font-family: 'Questrial', monospace;
        background:black;
        color:white;
        font-weight:lighter;
    }

    .return {
        padding-top:30px;
    }

    .return span {
        cursor: pointer;
    }

    .about-me-text p {
        text-align:left;
        width:60%;
        max-width:800px;
        margin:20px auto;
        font-family: 'Roboto Mono', monospace;
    }

    .about-me-text p a {
        font-weight: bolder;
        font-family: 'Questrial', monospace;
        text-decoration: none;
        font-size: 17px;
        color: white;
    }
</style>