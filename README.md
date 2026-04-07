<html>
<head>
  <title>Dreamers</title>
  <style> 
     body {
  background-image: url('background-loop.gif');
} </style>
  <link rel="icon" type="image/x-icon" href="icons/favicon.ico">
</head>
<body>
 <h1 style="color: white;">WELCOME TO YOUR DREAMs or .... nightmares</h1>
  <button onclick="typeWriter()">hey there</button>

<p id="demo"></p>

<script>
var i =0;
var txt = 'Find yourself in a world where its all jumbled';
var speed = 100;

function typeWriter() {
  if (i < txt.length) {
    document.getElementById("demo").innerHTML += txt.charAt(i);
    i++;
    setTimeout(typeWriter, speed);
  }
}
</script>
