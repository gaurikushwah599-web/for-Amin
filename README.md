# for-Amin
A little something for someone special ❤️
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Amin ❤️</title>

<style>
body {
  margin: 0;
  font-family: Arial;
  background: #0f0f0f;
  color: white;
  text-align: center;
}

.container {
  padding: 50px 20px;
}

button {
  margin: 10px;
  padding: 12px 20px;
  border-radius: 25px;
  border: none;
  cursor: pointer;
}

.yes {
  background: #ff4d6d;
  color: white;
}

.no {
  background: grey;
  color: white;
}

/* gift styles */
.gifts {
  display: none;
}

.gift-box {
  margin: 20px;
  padding: 20px;
  border: 2px dashed white;
  cursor: pointer;
}

/* vintage letter */
.letter {
  display: none;
  background: #f5deb3;
  color: #8b0000;
  padding: 30px;
  margin: 20px;
  font-family: cursive;
  border-radius: 10px;
}
</style>

</head>

<body>

<div class="container" id="main">

  <h1 id="question">Do you love me? ❤️</h1>

  <div id="buttons">
    <button class="yes" onclick="yes()">Yes</button>
    <button class="no" onclick="no()">No</button>
  </div>

</div>

<!-- Gifts Section -->
<div class="gifts" id="gifts">

  <h1>For you, Amin ❤️</h1>

  <div class="gift-box" onclick="showPhoto()">
    🎁 Gift 1 - Our Memory
  </div>

  <div class="gift-box" onclick="showSong()">
    🎶 Gift 2 - Our Song
  </div>

  <div class="gift-box" onclick="showLetter()">
    💌 Gift 3 - A Letter
  </div>

  <div id="photo" style="display:none;">
    <img src="https://photos.app.goo.gl/B4owx4Hx4wmHqHh76" width="250" style="border-radius:15px;">
  </div>

  <div id="song" style="display:none;">
    <p>Our song ❤️</p>
    <audio controls>
      <source src="https://youtu.be/nLnp0tpZ0ok?si=3bmSPtVQwbjHbf7f" type="audio/mpeg">
    </audio>
  </div>

  <div class="letter" id="letter">
    Amin,  
    no matter what happens between us,  
    you have a place in my heart that no one else can ever take.  
    You are not just someone I loved…  
    you are someone I still choose, quietly, every single day. ❤️
  </div>

</div>

<script>
let step = 0;

function yes() {
  document.getElementById("main").style.display = "none";
  document.getElementById("gifts").style.display = "block";
}

function no() {
  step++;

  if (step === 1) {
    document.getElementById("question").innerText = "Are you sure? 🥺";

    document.getElementById("buttons").innerHTML = `
      <button class="yes" style="font-size:22px;" onclick="yes()">Yes</button>
      <button class="no" style="font-size:12px;" onclick="no()">No</button>
    `;
  }

  else if (step === 2) {
    document.getElementById("question").innerText =
      "This is the last time I’m asking you… ❤️";

    document.getElementById("buttons").innerHTML = `
      <button class="yes" style="font-size:26px;" onclick="yes()">Yes</button>
    `;
  }
}

function showPhoto() {
  document.getElementById("photo").style.display = "block";
}

function showSong() {
  document.getElementById("song").style.display = "block";
}

function showLetter() {
  document.getElementById("letter").style.display = "block";
}
</script>

</body>
</html>
