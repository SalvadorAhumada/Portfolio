<template>
<section>
  <div class="video-background">

    <div class="video-foreground">
      <iframe src="https://www.youtube.com/embed/pcznaEKW7Ts?controls=0&showinfo=0&rel=0&autoplay=1&mute=1&loop=1&playlist=pcznaEKW7Ts" frameborder="0" allowfullscreen></iframe>
    </div>

  </div>

<div id="pattern-layer">
  <div class="main animated fadeIn delay-1s">
      <h1>Salvador Ahumada</h1>
      <p><a class="effect-2" href="#">about me</a></p>
  </div>
</div>
</section>
</template>

<script>
export default {

}
</script>

<style scoped>

*, *:before, *:after {
  box-sizing: border-box;
}

.main {
    width: 100%;
    height: 40vh;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    flex-direction: column;
}

.main h1 {
    font-family: 'Roboto Mono', monospace;
    color:black;
    margin:0;
    background:rgba(255, 255, 255, 0.795);
    padding:20px 40px;
    font-size:3rem;
}

.main p a {
    font-family: 'Roboto Mono', monospace; 
    font-size:1.3rem;
    cursor:pointer;
    transition:0.5s;
    color:white;
    text-decoration: none;  

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
data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAUAAAAFCAYAAACNbyblAAAALElEQVQYV2NkYGD4z8DAcJYBCTAyMDCcYWBgMEaWgAmC1MElkAXhEuiCYAkA3ioINdFY3lAAAAAASUVORK5CYII=
   ) repeat;
}

@media (min-aspect-ratio: 16/9) {
  .video-foreground { height: 300%; top: -100%; }
}
@media (max-aspect-ratio: 16/9) {
  .video-foreground { width: 300%; left: -100%; }
}
</style>