# p5-js-4<!DOCTYPE html>
<html lang="en">
  <head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.3/p5.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.3/addons/p5.sound.min.js"></script>
    <link rel="stylesheet" type="text/css" href="style.css">
    <meta charset="utf-8" />

  </head>
  <body>
    <main>
    </main>
    <script src="sketch.js"></script>
  </body>
</html>
let cor;// variavél cor
let posiçãoHorizontal;//x //variavél posição horizontal
let posiçãoVertical;//y //variavél posição vertical


function setup() { //preparar a tela
  
  createCanvas(400, 400);//criar cenário
  background(color(100, 0, 0)); //cor de fundo
  cor = color(random(0, 255), random(0, 255), random(0, 255)); // define a variavél cor
  posiçãoHorizontal = 200;//define a variável posição horizontal
  posiçãoVertical = 200;//define a variável posição vertical
}

function draw() {//desenhar a tela
 
  fill(cor);//preencher variável cor
  circle(posiçãoHorizontal, posiçãoVertical, 50);// faz um círculo
 
  
  if(mouseX < posiçãoHorizontal) {//se mouseX for menor que posição horizontal
    posiçãoHorizontal = posiçãoHorizontal - 1;//posição horizontal -1
  }
  
  if(mouseX > posiçãoHorizontal) {//se mouseX for maior que posição horizontal
    posiçãoHorizontal = posiçãoHorizontal + 1;// posição horizontal +1
  }
  
  if(mouseY < posiçãoVertical) {//se mouseY for menor que posição vertical
  posiçãoVertical--;//subtrai posição vertical
  }
  
  if(mouseY > posiçãoVertical) {// se mouseY for maior que posição vertical
    posiçãoVertical++;// adiciona posição vertical
 }
  
  if(mouseIsPressed) {// se mouse for pressionado
    cor = color(random(0, 255),random(0, 255),random(0, 255), random(0, 100));// muda variável cor
  }
}
