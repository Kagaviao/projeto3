# 3 bolas que atravessa a tela ⚽⚽⚽
let cor;
let circuloY;
let circuloX;

function setup() {
  createCanvas(400,400);
  background("red");
  cor=color(random(0,255),random(0,255),random(0,255));
  
circuloX = [0,0,0];
circuloY = [random(height),random(height),random(height)];
}

function draw() {
for(let quantos in circuloY) {
  circle(circuloX[quantos],circuloY[quantos],35);
  
  circuloX[quantos] += random(0,3);
  circuloY[quantos] += random(-3,3);
  
  if(circuloX[quantos]>= width){
    circuloX[quantos] = 0;
    circuloY[quantos] = random(height);
    
    
}
  
  
}
  fill (cor);
  
  
  
  if(mouseIsPressed){
 
  cor=color(random(0,255),random(0,255),random(0,255),random(0,225),random(0,100));
  }
  
    
    
}
