<html>
<head>
  <title>Dreamers</title>

  <style>
    body {
      background-image: url('background-loop.gif');
      background-size: cover;
      color: white;
      font-family: "Courier New", monospace;
      text-align: center;
      margin-top: 100px;
    }

    /* Typewriter cursor */
    #demo {
      border-right: 3px solid white;
      display: inline-block;
      padding-right: 5px;
      white-space: nowrap;
      overflow: hidden;
      animation: blink 0.7s step-end infinite;
    }

    @keyframes blink {
      50% { border-color: transparent; }
    }

    button {
      margin-top: 20px;
      padding: 10px 20px;
      background: black;
      color: white;
      border: 1px solid white;
      cursor: pointer;
    }
  </style>

  <link rel="icon" type="image/x-icon" href="icons/favicon.ico">
</head>

<body>

<h1>WELCOME TO YOUR DREAMs or .... nightmares</h1>

<button onclick="typeWriter()">hey there</button>

<p id="demo"></p>

<script>
var i = 0;
var txt = 'Find yourself in a world where its all jumbled';
var speed = 50;
var typing = false;

function typeWriter() {
  // Prevent overlapping typing if button clicked multiple times
  if (typing) return;

  typing = true;
  i = 0;
  document.getElementById("demo").innerHTML = ""; // reset text

  function type() {
    if (i < txt.length) {
      document.getElementById("demo").innerHTML += txt.charAt(i);
      i++;
      setTimeout(type, speed);
    } else {
      typing = false;
    }
  }

  type();
}
</script>

</body>
</html>
