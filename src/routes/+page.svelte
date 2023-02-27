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
          background-image: url("images/IMG_5841.jpg");
          background-position: center;
    background-size: cover;
      }
  

      .notepad{
        margin:auto;display:block;height:100vh;transform: rotate(2deg);position: fixed;
      }
      .menu-items{
        margin:auto;display:block;transform: rotate(3deg); top:40%;left: 48%;position:fixed;
      }
      .menu-item{
        display: block;
      }


      .notepad{
        margin:auto;display:block;height:100vh;transform: rotate(2deg);position: relative;
      }
      .shop-link{
        opacity: 1;
      }
      .archive-link{
        opacity:0.6
      }
      .comic-link{
        opacity:0.6
      }
      .about-link{
        opacity:0.6
      }

      .shop-link:hover{
        transform: rotate(-7deg);
      }
      .comic-link{
       transform: rotate(-3reg);
      }
      .about-link{
        transform: rotate(-9reg);
      }
      .archive-link{
        transform: rotate(4reg);
      }

      @media only screen and (max-width: 600px) {
        .notepad{
          margin-top: 30%;
          height:70vh;
          margin-right:2%;
        }
        .shop-link{
        height:7vh;top: -120px;left: 15%;
      }
      .archive-link{
        height:7vh;top: -120px;left: 15%;
      }
      .comic-link{
        height:7vh;top: -120px;left: 15%;
      }
      .about-link{
        height:7vh;top: -120px;left: 15%;
      }
}

  </style>
  
  
  <body transition:fade>
      <div class="cursor" style="height:100%;width:100%">
        <div style="position: relative; left: 0; top: 0;">
          <img src="images/homepage notepad seperate .png" alt="" class="notepad">

          <div class="menu-items">



            <div class="menu-item">
              <a href="/shop">
                <img src="images/result (1) (1).png" alt="" class="shop-link">
              </a>
            </div>

            <div class="menu-item">
              <a href="/comics">
                <img src="images/result (3) (1).png" alt="" class="comic-link">
              </a>
            </div>
            
            <div class="menu-item">
              <a href="/about">
                <img src="images/result (4) (1).png" alt="" class="about-link">
              </a>
            </div>

            <div class="menu-item">
              <a href="/archive">
                <img src="images/result (2) (1).png" alt="" class="archive-link">
              </a>
            </div>


          </div>
          
        </div>

          <img src="images/fronk-chicken-nightmares-3-5.gif" alt="test" style="height: 38vh;position: fixed;bottom: 0;z-index:10">
      </div>
  
  
  </body>