<template>
<section>
  <div class="video-background">

    <div class="video-foreground">
      <iframe src="https://www.youtube.com/embed/iGzOfXITytg?controls=0&showinfo=0&rel=0&autoplay=1&mute=1&loop=1&playlist=iGzOfXITytg" frameborder="0" allowfullscreen></iframe>
    </div>

  </div>

<div id="pattern-layer">
  <div class="main animated fadeIn delay-2s">
      <h1>Salvador Ahumada</h1>
      <p>Developer, designer and music addict.</p>
      <p>
        <a class="effect-2" @click='showMore()'>More about me
          <span class="material-icons">
            arrow_downward
          </span>
        </a>
      </p>
  </div>
</div>
  <transition
    name="custom-classes-transition"
    enter-active-class="animated slideInUp"
    leave-active-class="animated slideOutDown"
  >
    <aboutMe v-if= "show" v-on:close-modal="show =false"/> 
  </transition>
</section>
</template>

<script>
import aboutMe from "./about-me";
export default {
  components:{
    aboutMe
  },
  data() {
    return {
      show: false
    }
  },
  methods:{
    showMore() {
      this.show = true;
    }
  }
}
</script>

<style scoped>

*, *:before, *:after {
  box-sizing: border-box;
}

.main {
    width: 100%;
    height: 60vh;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    flex-direction: column;
}

.main h1 {
    font-family: 'Roboto Mono', monospace;
    margin:0;
    padding:20px 40px;
    font-size:3rem;
    transition:0.5s;
    color:white;
    background:none;
    border:1px solid white;
}

.music-video p {
      font-family: 'Roboto Mono', monospace;
      margin:0;
      font-size: 1.2rem;
      font-weight: bold;
}

.main h1:hover {
    background:rgba(255, 255, 255, 0.795);
    transition:0.5s;
    border:1px solid white;
    color:black;
}

.main p a {
    font-family: 'Roboto Mono', monospace; 
    font-size:1.3rem;
    cursor:pointer;
    transition:0.5s;
    color:white;
    text-decoration: none;  
}

.main p {
     font-family: 'Roboto Mono', monospace; 
    font-size:1.3rem; 
    margin: 0;
}

.main p a:hover {
    text-decoration: none;  
    transition:0.5s;
}


a, a > span {
  position: relative;
  color: inherit;
  text-decoration: none;
  line-height: 24px;
}
a:before, a > span:before, a:after, a > span:after {
  content: '';
  position: absolute;
  transition: transform 0.5s ease;
}

.effect-2 {
  padding: 10px;
  display: flex;
  flex-direction: column;
  height: 100px;
  justify-content: space-around;
}

.effect-2:before, .effect-2:after {
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  border-style: solid;
  border-color: #ffffff52;
}
.effect-2:before {
  border-width: 1px 0 1px 0;
  transform: scaleX(0);
}
.effect-2:after {
  border-width: 0 1px 0 1px;
  transform: scaleY(0);
}
.effect-2:hover:before, .effect-2:hover:after {
  transform: scale(1, 1);
}

section {
  width:100%;
  height:100%;
  position:relative;
}

* { box-sizing: border-box; }
.video-background {
  background: #000;
  position: fixed;
  top: 0; right: 0; bottom: 0; left: 0;
  z-index: -99;
}
.video-foreground,
.video-background iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
}
#pattern-layer {
    display:flex;
    align-items:center;
    justify-content:center;
    height:100%;
    color: #fff;
   background:url(
data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAYAAAAGCAYAAADgzO9IAAAAMElEQVQYV2NkYGA4w8DAsIUBDTAyMDA0MDAw+KBLwiRA6lEkkSVQJNEl4JLYJMCSAKd9CFN9zUF6AAAAAElFTkSuQmCC
   ) repeat;
}

@media (min-aspect-ratio: 16/9) {
  .video-foreground { height: 300%; top: -100%; }
}
@media (max-aspect-ratio: 16/9) {
  .video-foreground { width: 300%; left: -100%; }
}

@media screen and (max-width: 520px) {
  .main h1 {
    font-size: calc(25px + 6 * ((100vw - 320px) / 680));
    padding: 15px 30px;
  }

  .main p,
  .main p a {
    font-size: calc(15px + 6 * ((100vw - 320px) / 680));
    padding: 15px 30px;
  }
}
</style>