# projeto_b2
Projeto javascript 

#projeto-js Esse é um projeto simples, desenvolvido com html, css e javascript, de um semáforo que funciona ao acionar botões. O intuito é apresentar o conhecimemto adquirido de uma forma simples e prática.

Utilizei uma constante para receber a imagem do semáforo (const img) que ao clicar no botão das cores selecionadas -vermelho, amarelo e verde-, traga a imagem (const button). Aqui não irá capturar o objeto, mas sim o pai do objeto (div).
~~~javascript
const img = document.getElementById( "img" );
const buttons = document.getElementById( "buttons" );
~~~

Função "trafficLight" - irá receber o evento
~~~javascript
const trafficLight = (event) => {
  stopAutomatic();
  turnOn[event.target.id]();
}
~~~

Função changeColors -> mudar as cores 
~~~javascript
const changecolor = () => {
  const colors = ["red", "yellow", "green"]
  const color = colors[colorIndex];
  turnOn[color]();
  nextIndex();
}
~~~

Função (const nextIndex) -> terá a responsabilidade de ir para o próximo index (cor) Se for menor do que 2 (número 2 representando a posição da cor), aumenta mais um. Se não, o colorIndex volta ao 0. 

~~~javascript
const nextIndex = () => {
  if (colorIndex < 2) {
     colorIndex ++
  }else {
    colorIndex = 0;
  }
} 
~~~

Função (const) dentro de um objeto literal chamada "turnOn" "red" função vermelho - que troca a imagem para o vermelho,
"yellow" função amarelo - que troca a imagem para o amarelo, "green" função verde - que troca a imagem para o verde, "automatic" função automático - que troca as imagens para vermelho, verde e amarelo, ou seja, troca as cores (changeColor). O "setInterval" vai executar a função de mudar as cores a cada 1000 milisegundos. 
~~~javascript
const turnOn ={
  "red":    () => img.src = "img/vermelho.png",
  "yellow": () => img.src = "img/amarelo.png",
  "green":  () => img.src = "img/verde.png",
  "automatic":  () => intervalId = setInterval(changecolor, 1000)
}
~~~

buttons.addEventListener - ao clicar, captura o evento do 'trafficLight'.
~~~javascript
buttons.addEventListener("click",trafficLight);
~~~
