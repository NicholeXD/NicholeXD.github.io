<html><head><base href="https://sansundertale.com"><title>Sans' Skeleton Shenanigans</title>
<style>
  body {
    font-family: 'Comic Sans MS', cursive, sans-serif;
    background-color: #000000;
    color: #ffffff;
    margin: 0;
    padding: 0;
    overflow-x: hidden;
  }
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
  }
  header {
    text-align: center;
    padding: 20px 0;
    background-color: #0000FF;
    animation: glow 2s infinite alternate;
  }
  @keyframes glow {
    from { box-shadow: 0 0 10px #00FFFF; }
    to { box-shadow: 0 0 20px #00FFFF, 0 0 30px #00FFFF; }
  }
  h1 {
    font-size: 3em;
    margin: 0;
    text-shadow: 2px 2px #00FFFF;
  }
  .content {
    background-color: rgba(0, 0, 255, 0.1);
    border-radius: 10px;
    padding: 20px;
    margin-top: 20px;
  }
  .sans-sprite {
    width: 200px;
    height: 200px;
    background-image: url('sans_sprite.gif');
    background-size: cover;
    margin: 0 auto;
  }
  .pun {
    font-style: italic;
    color: #00FFFF;
    text-align: center;
    margin: 20px 0;
  }
  .sans-image {
    text-align: center;
    margin-top: 30px;
  }
  .sans-image img {
    max-width: 100%;
    border: 3px solid #00FFFF;
    border-radius: 10px;
  }
  footer {
    text-align: center;
    padding: 20px 0;
    background-color: #0000FF;
    margin-top: 20px;
  }
  #audio-controls {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: rgba(0, 0, 255, 0.5);
    padding: 10px;
    border-radius: 5px;
  }
  #sans-audio {
    display: block;
    margin: 20px auto;
  }
  #sans-video {
    display: block;
    margin: 20px auto;
    max-width: 100%;
    border: 3px solid #00FFFF;
    border-radius: 10px;
  }
</style>
</head><body>
<header>
  <h1>Sans' Skeleton Shenanigans</h1>
</header>

<div class="container">
  <div class="content">
    <h2>heya. i'm sans. sans the skeleton.</h2>
    <div class="sans-sprite"></div>
    <p>welcome to my little corner of the internet. i'm not really sure how i got here, but hey, when life gives you lemons, you make bad puns about them, right?</p>
    
    <div class="pun">"i've got a skele-ton of jokes for you!"</div>
    
    <h2>about me</h2>
    <p>i'm just a lazy bones from the underground. i like ketchup, taking naps, and telling jokes. oh, and i can teleport and decide your entire timeline. pretty cool, huh?</p>
    
    <div class="sans-image">
      <img src="https://i1.sndcdn.com/artworks-jyFyDWzqxzpf1d2I-LCHGpA-t500x500.jpg" alt="Sans with glowing blue eye on a black background, pixelated art style" width="500" height="500">
    </div>
    
    <audio id="sans-audio" controls>
      <source src="https://cdn.discordapp.com/attachments/1234687020706828329/1255598777159385170/Hey_kid_want_a_weiner_in_your_mouth_animated.mp3?ex=667db6fc&is=667c657c&hm=5267a01cc78cd894e50085401ba64aed7553322c0b35a72ab35952913c543f85&" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio>
    
    <h2>my favorite puns</h2>
    <ul>
      <li>why don't skeletons fight each other? they don't have the guts.</li>
      <li>i'm not lazy, i'm just bone idle.</li>
      <li>what do you call a fake noodle? an impasta!</li>
      <li>why did the skeleton go to the party alone? he had no body to go with!</li>
      <li>how does a skeleton call his friends? on his telebone!</li>
    </ul>
    
    <h2>random pun generator</h2>
    <p>need a quick laugh? click the button below and i'll tickle your funny bone!</p>
    <button onclick="generatePun()">Generate Pun</button>
    <p id="pun-display"></p>

    <h2>sans' special video</h2>
    <p>hey, check out this weird video i filmed in the underground. it's pretty humerus, don't you think? also buy my onlyfans</p>
    <video id="sans-video" controls>
      <source src="https://cdn.discordapp.com/attachments/1234687020706828329/1255597717934047262/chicos_estoy_comiendo_mortadela___original.mp4?ex=667db5ff&is=667c647f&hm=dff43cf01683055dfdc4073612892f22d4cedb1d2fe30d2e89090451a2771523&" type="video/mp4">
      Your browser does not support the video tag.
    </video>

  </div>
</div>

<footer>
  <p>© 20yomamashouse Sans | Professional Comedian and Nap Enthusiast</p>
</footer>

<div id="audio-controls">
  <button onclick="toggleAudio()">Toggle My Gym Playlist</button>
</div>

<script>
  const puns = [
    "Why don't skeletons fight each other? They don't have the guts.",
    "I'm not lazy, I'm just bone idle.",
    "What do you call a fake noodle? An impasta!",
    "Why did the skeleton go to the party alone? He had no body to go with!",
    "How does a skeleton call his friends? On his telebone!",
    "What's a skeleton's favorite instrument? The trombone!",
    "What do you call a skeleton who won't work? Lazy bones.",
    "Why don't skeletons like parties? They have no body to dance with.",
    "What do you call a skeleton snake? A rattler!",
    "Why didn't the skeleton cross the road? He didn't have the guts!",
    "What do you call a skeleton who works at a theme park? A roller ghoster!",
    "Why are skeletons so calm? Because nothing gets under their skin!",
    "What do you call a skeleton who won't get up in the morning? Lazy bones!",
    "Why don't skeletons fight each other? They don't have the stomach for it!",
    "What do you call a skeleton who presses charges? The plaintiff!",
    "Why did the skeleton go to the party? To get a little life into him!",
    "What do you call a skeleton who works at the beach? A life savor!",
    "Why don't skeletons play music in church? They have no organs!",
    "What do you call a skeleton who stays out in the snow? A numbskull!",
    "Why don't skeletons ever go trick or treating? Because they have nobody to go with!",
    "Why did the skeleton go to school? To improve his skull-astic skills!",
    "What do you call a skeleton who won't stop talking? A chatterbone!",
    "Why don't skeletons like winter? The cold goes right through them!",
    "What do you call a skeleton who tells jokes? A funny bone!",
    "Why don't skeletons play sports? They don't have the heart for it!"
  ];
  
  function generatePun() {
    const punDisplay = document.getElementById('pun-display');
    const randomPun = puns[Math.floor(Math.random() * puns.length)];
    punDisplay.textContent = randomPun;
  }

  const backgroundAudio = new Audio("https://cdn.discordapp.com/attachments/1234687020706828329/1255597108497481759/nicholovania.mp3_online-audio-converter.com.mp3?ex=667db56e&is=667c63ee&hm=ece6f568c9291b072c64710317ba2074a87b2648dbccb6f13e83394a1caf23e6&");
  backgroundAudio.loop = true;

  function toggleAudio() {
    if (backgroundAudio.paused) {
      backgroundAudio.play();
    } else {
      backgroundAudio.pause();
    }
  }

  // Start playing the background audio when the page loads
  window.onload = function() {
    backgroundAudio.play();
  }
</script>

</body></html>
