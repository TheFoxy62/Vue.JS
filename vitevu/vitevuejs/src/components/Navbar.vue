<script setup>
import { ref } from 'vue'

const Navbar = ref ('');
const propsUri = ref('https://pikariteshima.com/wp-content/uploads/2021/10/Komi.Cant_.Communicate.S01E04.Its_.Just_.a.Physical.Plus_.More_.1080p.NF_.WEB-DL.DDP2_.0.x264-NanDesuKa_001_32955-1024x576.png" height="300px" width="450px" alt="" />')


</script>

<template>
    <div class="topnav">
    <a class="active" href="#home">Home</a>
    <a href="#news">News</a>
    <a href="#contact">Contact</a>
    <a href="#about">About</a>
</div> 

<section class="grid">
    <div>
        <a href="#!">
            <img src="https://pikariteshima.com/wp-content/uploads/2021/10/Komi.Cant_.Communicate.S01E04.Its_.Just_.a.Physical.Plus_.More_.1080p.NF_.WEB-DL.DDP2_.0.x264-NanDesuKa_001_32955-1024x576.png" height="300px" width="450px" alt="" />
        </a>
        <div>
            <h5>Poster Komi Can't communicate!</h5>
            <details>14.99$</details>
            <button type="Click">Achat</button>
        </div>
    </div>
</section> 

</template>

<style>
body {
    margin: 0;
    font-family: Arial, Helvetica, sans-serif;
}

.topnav {
    overflow: hidden;
    background-color: rgb(48, 65, 160);
}

.topnav a {
    float: left;
    color: #f2f2f2;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
    font-size: 17px;
}

.topnav a:hover {
    background-color: #ddd;
    color: black;
}

.topnav a.active {
    background-color: #04AA6D;
    color: white;
}
.grid{
    grid-auto-columns: auto;
}

img:hover {
    animation: shake 0.5s;
    animation-iteration-count: infinite;
}

@keyframes shake {
    0% { transform: translate(1px, 1px) rotate(0deg); }
    10% { transform: translate(-1px, -2px) rotate(-1deg); }
    20% { transform: translate(-3px, 0px) rotate(1deg); }
    30% { transform: translate(3px, 2px) rotate(0deg); }
    40% { transform: translate(1px, -1px) rotate(1deg); }
    50% { transform: translate(-1px, 2px) rotate(-1deg); }
    60% { transform: translate(-3px, 1px) rotate(0deg); }
    70% { transform: translate(3px, 1px) rotate(-1deg); }
    80% { transform: translate(-1px, -1px) rotate(1deg); }
    90% { transform: translate(1px, 2px) rotate(0deg); }
    100% { transform: translate(1px, -2px) rotate(-1deg); }
}

</style>