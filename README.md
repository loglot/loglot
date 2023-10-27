<!--Hey! This is the original version
of Simple CSS Waves-->

<style>
@import url(//fonts.googleapis.com/css?family=Lato:300:400);

.background {
  position: fixed;
  top:0px;
  height: 100vh;
  width:  100vw;
  background : #4b4b4b; 
}

body {
  margin:0;
}

h1 {
  font-family: 'Lato', sans-serif;
  font-weight:300;
  letter-spacing: 2px;
  font-size:48px;
}
p {
  font-family: 'Lato', sans-serif;
  letter-spacing: 1px;
  font-size:14px;
  color: #333333;
}

.header {
  position:relative;
  text-align:center;
  background: linear-gradient(0deg, rgba(5,5,10,1) 0%, rgba(65,65,65,1) 100%);
  color:rgb(55,55,55);
}

.inner-header {
  height:65vh;
  width:100%;
  margin: 0;
  padding: 0;
}

.flex {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.waves {
  position:relative;
  width: 100%;
  height:15vh;
  margin-bottom:-7px;
  min-height:100px;
  max-height:150px;
}


.content {
  position:relative;
  /*height:20vh;*/
  text-align:center;
}


.parallax > use {
  animation: move-forever 25s cubic-bezier(.55,.5,.45,.5)     infinite;
}
.parallax > use:nth-child(1) {
  animation-delay: -2s;
  animation-duration: 7s;
}
.parallax > use:nth-child(2) {
  animation-delay: -3s;
  animation-duration: 10s;
}
.parallax > use:nth-child(3) {
  animation-delay: -4s;
  animation-duration: 13s;
}
.parallax > use:nth-child(4) {
  animation-delay: -5s;
  animation-duration: 16s;
}
.parallax > use:nth-child(5) {
  animation-delay: -6s;
  animation-duration: 19s;
}
.parallax > use:nth-child(6) {
  animation-delay: -7s;
  animation-duration: 30s;
}

@keyframes move-forever {
  0% {
   transform: translate3d(-90px,0,0);
  }
  100% { 
    transform: translate3d(85px,0,0);
  }
}

@media (max-width: 768px) {
  .waves {
    height:40px;
    min-height:40px;
  }
  .content {
    height:30vh;
  }
  h1 {
    font-size:24px;
  }
} 


body{
  display:flex;
  margin:0;
  padding:0;
  min-height: 100vh;
  /*background: #444;*/
  justify-content: center;
  align-items: center;
  font-family: arial;
}

.container{
  width: 90vw;

  display: flex;
  justify-content: space-between;
  flex-wrap:wrap;
  
}

.container .card{
  position: relative;
}

.container .card .face{
  width:300px;
  height: 200px;
  transition:.4s;
  
}

.container .card .face.face1{
  position: relative;
  background: linear-gradient(0deg, #333 0%, #2c2c2c 100%);
  display: flex;
  justify-content: center;
  align-content:center;
  align-items: center;
  z-index: 1;
  transform: translateY(100px);
}

.container .card:hover .face.face1{
  transform: translateY(0);
  box-shadow:
    inset 0 0 60px whitesmoke,
    inset 20px 0 80px rgb(255, 0, 0),
    inset -20px 0 80px rgb(255, 255, 0),
    inset 20px 0 300px rgb(255, 0, 0),
    inset -20px 0 300px rgb(255, 255, 0),
    0 0 50px #fff,
    -10px 0 80px rgb(255, 0, 0),
    10px 0 80px rgb(255, 255, 0); 
   
}


.container .card .face.face1 .content{
  opacity: .2;
  transition:  0.5s;
  text-align: center;
  
}

.container .card:hover .face.face1 .content{
  opacity: 1;
 
}

.container .card .face.face1 .content i{
  font-size: 3em;
  color: white;
  display: inline-block;
   
}

.container .card .face.face1 .content h3{
  font-size: 1em;
  color: white;
  text-align: center;
  
}

.container .card .face.face1 .content a{
   transition: .5s;
}

.container .card .face.face2{
   position: relative;
   background: linear-gradient(0deg, rgba(50,50,50,0) 0%, 	rgba(51, 51, 51, 0) 75%);;
   display: flex;
   align-items: center;
   justify-content: center;
   padding: 20px;
  box-sizing: border-box;
  box-shadow: 0 20px 50px rgba(0,0,0,.8);
  transform: translateY(-100px);
  backdrop-filter: blur(10px);
}

.container .card:hover .face.face2{
    transform: translateY(0);


}

.container .card .face.face2 .content p, a{
  font-size: 10pt;
  margin: 0 ;
  padding: 0;
  color:#ccc;
}

.container .card .face.face2 .content a{
  text-decoration:none;
  color: #ccc;
  box-sizing: border-box;
  outline : 1px dashed #ccc;
  padding: 10px;
  margin: 15px 0 0;
  display: inline-block;
}

.container .card .face.face2 .content a:hover{
  color: rgb(255, 255, 255); 
  box-shadow: inset 0px 0px 10px rgba(0,0,0,0.5);
}
.scroll {

  position: absolute; 
}

.gradient {
  width : 100vw;
  height : 50vh;
  background:  linear-gradient(0deg, rgb(20, 20, 20) 0%, rgba(50,50,50,0) 75%);
  top : 50%;
  position: fixed;
  pointer-events: none;
}
</style>

<div class="background">
    <div class="header">
        <div>
        <svg class="waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
        viewBox="0 24 150 28" preserveAspectRatio="none" shape-rendering="auto">
        <defs>
        <path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z" />
        </defs>
        <g class="parallax">
        <use xlink:href="#gentle-wave" x="48" y="-5" fill="rgba(25,25,25,1)" />
        <use xlink:href="#gentle-wave" x="48" y="-3" fill="rgba(35,35,35,1)" />
        <use xlink:href="#gentle-wave" x="48" y="0" fill="rgba(45,45,45,1" />
        <use xlink:href="#gentle-wave" x="48" y="3" fill="rgba(55,55,55,1)" />
        <use xlink:href="#gentle-wave" x="48" y="5" fill="rgba(65,65,65,1)" />
        <use xlink:href="#gentle-wave" x="48" y="7" fill="rgba(75,75,75,1)" />
        </g>
        </svg>
        </div>
      </div>
    </div>
        <head>
        <title>loglot home</title>
        </head>
        <body>
             <script src="https://kit.fontawesome.com/95a02bd20d.js">
             </script>
          <div class="container" order: 10>
             <div class="card">
               <div class="face face1">
                 <div class="content">
                    <svg id="ecdaNrmeyOh1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 300 130" shape-rendering="geometricPrecision" text-rendering="geometricPrecision"><rect width="121.559298" height="261.770552" rx="60.78" ry="60.78" transform="matrix(.429112 0 0 0.429112 123.918723 12.796025)" fill="rgba(210,219,237,0)" stroke="#fff" stroke-width="15"/></svg>
                    <h3>Yet Another 2d Platformer</h3>
                 </div>
               </div>
               <div class="face face2">
                 <div class="content">
                   <p> the game i am actively working on (when i'm not working on things like this website, or playing games), made as a sequal in gameplay to demo 0.4</p>
                   <a href="https://loglot.github.io/yet-another-2d-platformer/" type="button">Play Game</a>
                 </div>
               </div>
            </div>
            <div class="card">
               <div class="face face1">
                 <div class="content">
                    <svg id="ecXREiLwJGa1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 300 150" shape-rendering="geometricPrecision" text-rendering="geometricPrecision"><ellipse rx="69.784042" ry="69.784042" transform="matrix(.768937 0 0 0.768937 120.677304 87.401931)" fill="rgba(210,219,237,0)" stroke="#fff" stroke-width="10"/><ellipse rx="37.464705" ry="37.464705" transform="matrix(.426083 0 0 0.426083 190.29991 33.742399)" fill="rgba(210,219,237,0)" stroke="#fff" stroke-width="10"/></svg>
                <h3>Yet Another Collectathon</h3>
                </div>
               </div>
               <div class="face face2">
                 <div class="content">
                   <p> <br><br> This is the first javascript game i've made, very simple, very bad</p>
                   <a href="https://loglot.github.io/Yet-Another-Collectathon/" type="button">Play Game</a>
                 </div>
               </div>
            </div>
            <div class="card">
               <div class="face face1">
                 <div class="content">
                    <svg id="e4YEs2e8H1p1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 300 300" shape-rendering="geometricPrecision" text-rendering="geometricPrecision"><ellipse rx="145.962677" ry="145.962677" transform="matrix(.913055 0 0 0.913055 150 150)" fill="rgba(0,0,0,0)" stroke="#fff" stroke-width="30"/><rect width="124.349543" height="23.497219" rx="11.75" ry="11.75" transform="matrix(.945022 0 0 1.196104 7.455568 135.947442)" fill="#fff" stroke-width="0"/></svg>
                    <h3>demo 0.4</h3>
                 </div>
               </div>
               <div class="face face2">
                 <div class="content">
                   <p> this was the first game i've made, it was never finished... hence the title, the code got terrible to expand, so i stopped</p>
                   <a href="https://loglot.github.io/abandoned-game/" type="button">Play Game</a>
                 </div>
               </div>
            </div>
            <div class="card">
                <div class="face face1">
                  <div class="content">
               <i class=>></i>               
                 <h3>Read More</h3>
                 </div>
                </div>
                <div class="face face2">
                  <div class="content">
                    <p><br><br> i have a blog! it gets updated when it gets updated</p>
                    <a href="https://loglotgamedev.wordpress.com/" type="button">Go To Blog</a>
                  </div>
                </div>
              </div>
          </div>
        </body>
        <div class="gradient"></div>

<!--
**loglot/loglot** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
