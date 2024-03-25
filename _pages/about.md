---
title: "Hi I'm zkvlkat 😎"
permalink: /about/
layout: single
comments: false
---

<div>
    <img src="/assets/images/coon.jpg" alt="about_meee" width="70%" min-width="700px" itemprop="image">
</div>

<div class="container">
    <div class="overlay"></div>
    <div class="card"></div>
</div>
<script>
var container = document.querySelector('.container');
var overlay = document.querySelector('.overlay');
container.addEventListener('mousemove',function(e){
    var x = e.offsetX
    var y = e.offsetY
    //console.log(x,y);
    var rotateY = -1/5 * x + 20
    var rotateX = 4/30 * x - 20

    overlay.style = `background-position : ${x/5 + y/5}` 

    container.style = `transform : perspective(350px) rotateY(${rotateY}deg)
    rotateX(${rotateX}deg)`

    container.addEventListener('mouseout',function(){
        overlay.style = 'filter : opacity(0)'
        container.style = 'transform : perspective(350px) rotateY(0deg) rotateX(0deg)'
    })
})
</script>
<style>
    .container {
        width: 220px; height: 310px;
    }
    .overlay{
        position : absolute;
        width: 220px;
        height: 310px;
        background: linear-gradient(105deg,
        transparent 40%,
        rgba(255,219,112,0.8) 45%,
        rgba(132,50,255,0.6) 50%,
        transparent 54%);
        background-size: 150% 150%;
        background-position: 100%;
        filter: brightness(1.1) opacity(0.8);
        mix-blend-mode: color-dodge;
        transition: all 0.1s;
    }
    .card {
        width: 220px; height: 310px;
        background-image :url(/assets/images/coon.jpg);
        background-size: cover;
    }
    </style>

<div style="border-left: 2px solid rgba(199, 198, 198, 0.7); margin: 0.5em 0 0 0.5em; padding-left: 1.5em; font-weight: 500;">
    <ul class="author__urls social-icons">
        <li itemprop="homeLocation" itemscope itemtype="https://schema.org/Place">
          <i class="fas fa-fw fa-map-marker-alt" aria-hidden="true"></i> <span itemprop="name">  Korea</span>
        </li>
        <li>
          <a href="https://github.com/zkvlkat" itemprop="sameAs" rel="nofollow noopener noreferrer">
            <i class="fab fa-fw fa-github" aria-hidden="true"></i><span class="label">  https://github.com/zkvlkat</span>
          </a>
        </li>
        <li>
          <a href="mailto:aa740700@gmail.com">
            <meta itemprop="email" content="aa740700@gmail.com" />
            <i class="fas fa-fw fa-envelope-square" aria-hidden="true"></i><span class="label">  aa740700@gmail.com</span>
          </a>
        </li>
        <li>
          <a href="https://www.instagram.com/" itemprop="sameAs" rel="nofollow noopener noreferrer">
            <i class="fab fa-fw fa-instagram" aria-hidden="true"></i><span class="label">  https://www.instagram.com/</span>
          </a>
        </li>
    </ul>
  </div>
