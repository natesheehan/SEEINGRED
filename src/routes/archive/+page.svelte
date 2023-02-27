<script>
  import { fly } from "svelte/transition";
</script>

<style>


  .menu-item{
          display:inline !important;
        }
        .logo-link{
          height: 10vh;
        }
  </style>
<body transition:fly="{{ x: 200, duration: 2000 }}">
  
  <div class="menu-items">

      <div class="menu-item">
          <a href="/">
            <img src="images/sr-log.png" alt="" class="logo-link">
          </a>
        </div>

    </div>
</body>