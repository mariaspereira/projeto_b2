# projeto_b2
Projeto javascript 

#projeto-js Esse é um projeto simples, desenvolvido com html, css e javascript, de um semáforo que funciona ao acionar botões. O intuito é apresentar o conhecimemto adquirido de uma forma simples e prática.

Utilizei uma constante para receber a imagem do semáforo (const img) que ao clicar no botão das cores selecionadas -vermelho, amarelo e verde-, traga a imagem (const button). Aqui não irá capturar o objeto, mas sim o pai do objeto (div). https://user-images.githubusercontent.com/103434769/172631634-0bd0baa0-ba58-446d-a567-4cfe3ed6f89b.PNG

Função "trafficLight" - irá receber o evento https://user-images.githubusercontent.com/103434769/172632938-62183f23-f3cb-4e17-9e8c-194fc1cafc9f.PNG

Função changeColors -> mudar as cores https://user-images.githubusercontent.com/103434769/172636684-4a9fa6c6-0197-4063-8e68-06e7e5e4c66b.PNG

Função (const nextIndex) -> terá a responsabilidade de ir para o próximo index (cor) Se for menor do que 2 (número 2 representando a posição da cor), aumenta mais um. Se não, o colorIndex volta ao 0. https://user-images.githubusercontent.com/103434769/172639195-6f17f2cb-c79a-482e-bce2-6e6d53803ae9.PNG

Função (const) dentro de um objeto literal chamada "turnOn" "red" função vermelho - que troca a imagem para o vermelho,
"yellow" função amarelo - que troca a imagem para o amarelo, "green" função verde - que troca a imagem para o verde, "automatic" função automático - que troca as imagens para vermelho, verde e amarelo, ou seja, troca as cores (changeColor). O "setInterval" vai executar a função de mudar as cores a cada 1000 milisegundos. https://user-images.githubusercontent.com/103434769/172635980-c4f57e9b-33cf-42dc-8ee6-0f33f3413dfb.PNG

buttons.addEventListener("click", trafficLight) - ao clicar, captura o evento do 'trafficLight'.
