<template>
<div class="title-bar" style="margin:30px">
  <div class="title-bar-text">DFlowProductions</div>
  <div class="title-bar-controls">
    <button aria-label="Minimize"></button>
    <button aria-label="Maximize"></button>
    <button aria-label="Close"></button>
  </div>
</div>
<div class="centered">
    <button onclick="window.location.href='#/';">Home</button>
    <button onclick="window.location.href='#/game';">Game Dev</button>
    <button onclick="window.location.href='#/series';">Series</button>
    <button onclick="window.location.href='#/edit';">Edit</button>
  <component :is="currentView" />
</div>

<div class="centered">
<div class="window" style="width: 600px;margin:30px">
  <div class="title-bar">
    <div class="title-bar-text">What's This???</div>
  </div>
  <div class="window-body">
<p> Welcome To My Editing Page!</p>
<ul>
    <li>Professional Editing Services</li>
    <li>Years Of Experience In Davinci Resolve And Adobe Premiere Pro/After Effects</li>
    <li>Long Form And Short Form Content</li>
</ul>
  </div>
  <div class="status-bar">
    <p class="status-bar-field">Press F1 for help</p>
    <p class="status-bar-field">Slide 4</p>
    <p class="status-bar-field">CPU Usage: 42%</p>
  </div>
</div>
</div>

<div class="centered">
  <div class="window" style="width: 600px;margin:30px">
  <div class="title-bar">
    <div class="title-bar-text">The Things!</div>
    <div class="title-bar-controls">
      <button aria-label="Minimize"></button>
      <button aria-label="Maximize"></button>
      <button aria-label="Close"></button>
    </div>
  </div>
  <div class="window-body">
  <p>[EDITING WORK FOR YOUTUBE CONTENT CREATORS]</p>
  <a href="https://youtu.be/3nQaxsUFVj4?si=51tMEO1DapzVUc2H"> <img src="/public/DAY.png"> </a>
  <br>
  <a href="https://www.tiktok.com/@dionysusflow?lang=en"> <img src="/public/DIO.png"> </a>
  <br>
  <a href="https://www.youtube.com/watch?v=i_MwuOnOnpU"> <img src="/public/KEYSMASH.png"> </a>
  <br>
  <p>[Video And Audio Editing And Production In SCP RAISA]</p>
  <a href="https://www.youtube.com/@DFlowProds"> <img src="/public/RAISA.png"> </a>
  <br>
  </div>
</div>
</div>

<footer>  
  <a href="https://x.com/DFlowProds"> <img src="/public/twitter.svg"> </a>
  <a href="https://bsky.app/profile/dflowproductions.bsky.social"> <img src="/public/bluesky.svg"> </a>
  <a href="https://www.linkedin.com/in/reece-beattie-3573813aa/"> <img src="/public/linkedin.svg"> </a>
  <a href="https://www.twitch.tv/dflowproductions"> <img src="/public/twitch.svg"> </a>
  <a href="mailto:dflowprods@gmail.com"><img src="/public/mail.svg"></a> 
  <a href="https://www.youtube.com/@DFlowProds"> <img src="/public/youtube.svg"> </a>
</footer>

</template>

<script setup>
</script>

<style>
  body{
    background-image: url('background.png');
    background-size: cover;  
  }

  img {
    display: block;
    width: 500px;
    margin: 0 auto;
    object-fit: cover; /* or contain, fill, none, scale-down */
}
  .centered { 
  display: flex; 
  justify-content: center; 
  align-items: center; 
}

  footer {
    display: flex;
    justify-content: flex-end;
    gap: 5px;
  }

  footer img {    
    width: 30px;
    display: inline-block;
    margin: 0;
    object-fit: cover;
  }
</style>