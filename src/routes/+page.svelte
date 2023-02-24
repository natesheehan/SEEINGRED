<script>
  import { fade } from "svelte/transition";
  import { browser } from "$app/environment";
  if(browser) {
      const cursor = document.querySelector('.cursor');
  
  const moveCursor = (e)=> {
    const mouseY = e.clientY;
    const mouseX = e.clientX;
     
    cursor.style.transform = `translate3d(${mouseX}px, ${mouseY}px, 0)`;
    
  }
  window.addEventListener('mousemove', moveCursor)
  
  }
  
  </script>
  <style>

      body {
        overflow: hidden;
        cursor:grab;
          background-color: #d6d6d6;
          background-image: url("images/logo.png");
    background-repeat: repeat;
    background-size: 18vh;
      }
      .cursor{
          background-image: url("images/cursor for website.png");
      }
  </style>
  
  
  <body transition:fade>
      <div class="cursor" style="height:100%;width:100%">
        <div style="position: relative; left: 0; top: 0;">
          <img src="images/notepad.png" alt="" style="margin:auto;display:block;height:100vh;transform: rotate(2deg);position: relative;">
          <img src="images/result (1).png" alt="" style="margin:auto;display:block;height:70vh;transform: rotate(7deg); top: -120px;left: 35%;position:fixed">
          <img src="images/result (2).png" alt="" style="margin:auto;display:block;height:70vh;transform: rotate(3deg); top:0px;left: 35%;position:fixed;opacity:0.4">
          <img src="images/result (3).png" alt="" style="margin:auto;display:block;height:70vh;transform: rotate(9deg); top: 120px;left: 35%;position:fixed;opacity:0.4">
          <img src="images/result (4).png" alt="" style="margin:auto;display:block;height:70vh;transform: rotate(4deg); top: 240px;left: 35%;position:fixed;opacity:0.4">
        </div>

          <img src="images/fronk-chicken-nightmares-3-5.gif" alt="test" style="height: 38vh;position: fixed;bottom: 0;">
      </div>
  
  
  </body>