<script>
	import { browser } from "$app/environment";
  import { fade } from "svelte/transition";
  if(browser){
    const gallery = document.getElementById("gallery");

window.onmousemove = e => {
  const mouseX = e.clientX,
        mouseY = e.clientY;
  
  const xDecimal = mouseX / window.innerWidth,
        yDecimal = mouseY / window.innerHeight;
  
  const maxX = gallery.offsetWidth - window.innerWidth,
        maxY = gallery.offsetHeight - window.innerHeight;
  
  const panX = maxX * xDecimal * -1,
        panY = maxY * yDecimal * -1;
  
  gallery.animate({
    transform: `translate(${panX}px, ${panY}px)`
  }, {
    duration: 4000,
    fill: "forwards",
    easing: "ease"
  })
  }



}
</script>
<style>
 :global(body){
  background-image: url("/images/background for website.png");
  background-size: 200vh;;
  height: 50vh;  
  margin: 0px;
  overflow: hidden;
 }


#gallery {
  height: 140vmax;
  width: 140vmax;  
  position: absolute;
}

.tile {
  border-radius: 1vmax;
  position: absolute;
  transition: transform 800ms ease;
}

.tile:hover {
  transform: scale(1.1);
}

.tile:hover > img {
  opacity: 1;
  transform: scale(1.01);
}

.tile > img {
  height: 100%;
  width: 100%;
  object-fit: cover;
  border-radius: inherit;
  opacity: 0;
  transition: opacity 800ms ease,
    transform 800ms ease;
}

.tile:nth-child(1) {
  background-image: url("/images/coming soon.png");
  height: 18%;
  width: 20%;
  left: 5%;
  top: 5%;
}

.tile:nth-child(2) {
  background-image: url("/images/coming soon.png");
  height: 28%;
  width: 18%;
  left: 42%;
  top: 12%;
}

.tile:nth-child(3) {
  background-image: url("/images/coming soon.png");
  height: 16%;
  width: 12%;
  left: 12%;
  top: 34%;
}

.tile:nth-child(4) {
  background-image: url("/images/coming soon.png");
  height: 18%;
  width: 14%;
  left: 45%;
  top: 48%;
}

.tile:nth-child(5) {
  background-image: url("/images/comic book drawings 1.png");
  height: 16%;
  width: 12%;
  left: 8%;
  top: 70%;
}

#source-link {
  bottom: 60px;
}

#source-link > i {
  color: rgb(94, 106, 210);
}


.meta-link {
  align-items: center;
  backdrop-filter: blur(3px);
  background-color: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 6px;
  bottom: 10px;
  box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.1);
  cursor: pointer;  
  display: inline-flex;
  gap: 5px;
  left: 10px;
  padding: 10px 20px;
  position: fixed;
  text-decoration: none;
  transition: background-color 400ms, border-color 400ms;
  z-index: 10000;
}

.meta-link:hover {
  background-color: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.meta-link > i, .meta-link > span {
  height: 20px;
  line-height: 20px;
}

.meta-link > span {
  color: white;
  font-family: "Rubik", sans-serif;
  font-weight: 500;
}

:global(h1,p){
  font-family: Gloria Hallelujah ;
}
</style>
<svelte:head>
    <style>
        @import url("https://fonts.googleapis.com/css2?family=Gloria+Hallelujah&family=Space+Mono:wght@400;700&display=swap");
    </style>
</svelte:head>
<body transition:fade>
  
<div id="gallery">
  <div class="tile">
    <img src="/images/coming soon.png" />
  </div>
  <div class="tile">
    <img src="/images/coming soon.png" />
  </div>
  <div class="tile">
    <img src="/images/coming soon.png" />
  </div>
  <div class="tile">
    <img src="/images/coming soon.png" />
  </div>
  <div class="tile">
    <img src="/images/comic book drawings 1.png" />
    Comics
  </div>

<a data-sveltekit-preload-data="tap" href="/comics">
  <h1>COMICS</h1>
</a>
</div>

<a id="source-link" class="meta-link" href="https://palette.supply" target="_blank">
  <i class="fa-solid fa-instagram"></i>
  <span>Instagram</span>
</a>


</body>