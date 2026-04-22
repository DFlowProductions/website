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
<div class="window" style="width: 600px;margin:30px">
  <div class="title-bar">
    <div class="title-bar-text">Where Are We???</div>
  </div>
  <div class="window-body">
<p> This Is My Website!</p>
<ul>
    <li>My Portfolio</li>
    <li>Showcase Of Cool Things I Made</li>
    <li>And A Snazzy Windows 98 Themed Thing</li>
</ul>
  </div>
  <div class="status-bar">
    <p class="status-bar-field">Press F1 for help</p>
    <p class="status-bar-field">Slide 1</p>
    <p class="status-bar-field">CPU Usage: 42%</p>
  </div>
</div>
</div>

<div class="centered">
  <div class="window" style="width: 600px;margin:30px">
  <div class="title-bar">
    <div class="title-bar-text">Some Cool Projects!</div>
    <div class="title-bar-controls">
      <button aria-label="Minimize"></button>
      <button aria-label="Maximize"></button>
      <button aria-label="Close"></button>
    </div>
  </div>
  <div class="window-body">
  <p>[GODOT CHARACTER CONTROLLER]</p>
  <a href="https://dflowproductions.itch.io/player-controller-and-various-shaders-test"> <img src="/public/CharacterController.png"> </a>
  <br>
  <p>[SCP HORROR AUDIO DRAMA SERIES]</p>
  <a href="https://www.youtube.com/@DFlowProds"> <img src="/public/RAISA.png"> </a>
  <br>
  </div>
</div>
</div>

<div class="centered">
  <div class="window" style="width: 600px;margin:30px">
  <div class="title-bar">
    <div class="title-bar-text">Cookie Clicker Gambler!</div>
    <div class="title-bar-controls">
      <button aria-label="Minimize"></button>
      <button aria-label="Maximize"></button>
      <button aria-label="Close"></button>
    </div>
  </div>
  <div class="window-body">
  <p>Cookies Clicked: {{ counter }}</p>
  <button @click="increase">Add a Cookie!</button>
  <button @click="gamble">Gamble a Cookie!</button>
  </div>
</div>
</div>

</template>

<script setup>

  import {ref} from "vue";

  const counter = ref()

  function increase(){
    counter.value = JSON.parse(localStorage.getItem('myInteger'));
    counter.value++
    localStorage.setItem('myInteger', JSON.stringify(counter.value));
  }
  function gamble(){
    counter.value = JSON.parse(localStorage.getItem('myInteger'));
    var i = Math.floor(Math.random() * 10 + 1)
    if (i==10){
      counter.value+=20
    }else{
      counter.value--
    }
    localStorage.setItem('myInteger', JSON.stringify(counter.value));
    
  }

  

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
</style>