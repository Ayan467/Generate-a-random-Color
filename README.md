# Generate-a-random-Color
This is my first mini repo using  HTML CSS &amp; JS

#HTML CODE
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <h3>Generate a random color</h3>
  <br>
<button>generate color</button>
<br>
<br>
<div>This is your new color</div>

  <script src="index.js"></script>
</body>
</html>


#CSS CODE

body {
    text-align: center;
}

div {
    height: 100px;
    width: 500px;
    border :1px solid black;
    margin: auto;
}

#JS CODE

let btn = document.querySelector("button");

btn.addEventListener("click", function() {
   let h3 = document.querySelector("h3");
   let randomColor = getRandomColor();
   h3.innerText = randomColor;
   console.log('color updated');

   let div = document.querySelector("div");
   div.style.backgroundColor = randomColor;
});

function getRandomColor() {
    let red = Math.floor(Math.random() * 255);
    let green = Math.floor(Math.random() * 255);
    let blue = Math.floor(Math.random() * 255);

    let color = `rgb(${red}, ${green}, ${blue})`;
    return color;
}
