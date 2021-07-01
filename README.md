# Laboratorio_01
Como os valores negativos são codificados? Os valores negativos são codificados utilizando as intruções normais, com números binários, 
como por exemplo no execico 1 que quando é feito o comando: MOV R2, #-1 o resultado é 0xffff'ffff, ou seja o contrario do que acontece 
em MOV R0, #0, em que o resulado é 0x0000'0000. É possível visualizar os estados individuais dos flags? Sim é possível utilizar os estados 
individuais de flags utilizando a extensão S as intruções, que então resulta em 1 quando as condições N,Z ou C são verdadeiras, sendo o N negação,
Z de zero, ou seja o valor do endereço é igual a 0, e C que é o carry out.
Como o PC está relacionaod à janela Disassembly? O PC está relacionado à janela Disassembly, pois o PC mostra o endereço da próxima instrução que
deve ser feita. A janela Disassembly é a janela que vemos grifado em verde a próxima instrução. Portanto é dessa forma que os dois (PC e Disassembly)
se relacionam. Quais intruções são de 16 bits e quais são de 32? As intruções de 16 bits são descritas na janela disassembly com apenas 4 bits como
por exemplo: 0xe7e6, enquanto as de 32 bits são descritas com 8 bits como por exemplo: 0xf04f 0x0055. Os mnemônicos do disassembly correspondem exatamente
aos mnemônicos usados no programa? Sim, os mnemônicos usados na programação são iguais aos mnemônicos que aparecem na janela disassembly. A construção da
aplicação foi bem sucedida? Não, a construção não foi bem sucedida, pois os comandos não ocorrem com esperado, como por exemplo o MVN R1,R0, LSL#16 deu 
um resultado de 0x0055'ffff, quando o esperado era 0x0000'ffff.

Procure decifrar os resultados de cada operação. O comando MOV R0, #0x55 resulta em 0x0000'0055, ou seja é setado como valor inicial para o R0 de 
0x0000'0055 (0x55) O comando MOV R1, R0, LSL#16 significa que o progrma vai pegar o valor de R0, mover o seu valor 16 bits para a direita e esse será o valor
de R1, o que resulta em 0x0055'0000. O comando R2, R1, LSR #8 significa que o progrma vai pegar o valor de R1, mover seu valor 8 bits para a esquerda para o 
R2,o que resulta em 0x0000'5500. O comando MOV R3, R2, ASR #4 que pega o valor de R1, mmover seu valor em 4 bits para a esquerda, que resulta em 0x0000'0550. 
O comando MOV R4, R3, ROR #2 essa instrução pega o valor em binário de R3 que é 550 em hexadecimal, rotaciona os dois ultimos bits e os dois primeiros bits
o que gera o 154 em binario e nos da o resuldade de R4 que é 0x0000'0154. O comando R5, R4, RRX ... No exercicio também foi pedido para substituir a instrção
MOV pela instrução MVN que é a negação da função MOV, portanto o que ele fará é o contrário do que as instruções MOV. Como: A isntrução MVN R6, #0x55 irá setar
como valor inicial não 0x55, que da 0xffff'ffaa. A instrução MVN R7, R6, LSL#16 ira mover o valor de R6 16 bits para a direita, ou seja deveriamos ter 0x0000'ffff,
quando na realidade temos 0x0055'ffff.
