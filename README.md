# Seatwork-9-15-25
Application of JavaScript 
<!DOCTYPE html>
<html>
<head>
  <title>Button Alert</title>
  <style>
    h1{
        text-align: center;
        color:black;
        font-family: 'Times New Roman', Times, serif;
    }
    body{
        color: lightcoral;
        font-family: 'Courier New', Courier, monospace;
        background-color: blanchedalmond;
    }
    button {
      padding: 10px 20px;
      background: rgb(198, 192, 157);
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      color: black;
    }
    button:hover {
      background: maroon;
    }
     .gallery {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 10px;
    }

    .gallery img {
      width: 150px;
      height: 100px;
      object-fit: cover;
      border-radius: 5px;
      cursor: pointer;
      transition: transform 0.2s;
    }

    .gallery img:hover {
      transform: scale(1.05);
    }

    /* Lightbox (big image view) */
    .lightbox {
      display: none;
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.8);
      justify-content: center;
      align-items: center;
    }

    .lightbox img {
      max-width: 80%;
      max-height: 80%;
      border-radius: 10px;
    }

    .controls {
      position: absolute;
      top: 50%;
      width: 100%;
      display: flex;
      justify-content: space-between;
      color: white;
      font-size: 2em;
      cursor: pointer;
      padding: 0 30px;
      user-select: none;
    }

    .close {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 2em;
      cursor: pointer;
      color: white;
    }
  </style>
</head>
<body>
<h1>Welcome to JavaScript </h1>
<br>
  <h2>Time and Date </h2>
  <button type="button" onclick="document.getElementById('demo').innerHTML=Date()">
    Show Date and Time </button>
    <p id="demo"></p>
    <br>
<h3>What can JavaScript Do?</h3>
<p id="memo">JavaScript is the programming language of the web.
It can update and change both HTML and CSS.
It can calculate, manipulate and validate data.</p>
<button type="button" onclick='document.getElementById("memo").innerHTML="JavaScript Can be integreated in CSS and HTML"'>More Info!</button>
<br>
  <h2>Show Message</h2>
  <button onclick="showMessage()">Click Me</button>
  <script>
    function showMessage() {
      alert("Hello! You clicked the button.");
    }
  </script>
<h4>Photo Gallery</h4>
<div class="gallery">
    <button onclick="document.getElementById('myImage').src='https://picsum.photos/id/1015/400/300'">Prev</button>
    <img id="myImage"src="https://picsum.photos/id/1035/400/300" alt="pic3" onclick="openLightbox(2)">
<img id="myImage"src="https://picsum.photos/id/1045/400/300" alt="pic3" onclick="openLightbox(2)">
<button onclick="document.getElementById('myImage').src='https://picsum.photos/id/1035/400/300'">Next</button>

  </div>

</body>
</html>
