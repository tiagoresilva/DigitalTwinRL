# Introdução 

Segue a seguir o passo a passo para treinamento e testes da garra manipuladora de latas.Este sistema consiste em coletar latas transportadas por uma esteira de alimentação e posicioná-las em uma caixa numa segunda esteira. É composta por uma garra, um motor que se movimenta no eixo x e outro motor que se movimenta no eixo y. Cabe a essa máquina preencher 3 fileiras com 3 latas na caixa, sem deixar que as latas batam umas nas outras ou batam em obstáculos, sem realizar a captura das latas quando qualquer uma das esteiras esteja em movimento. A cada fileira preenchida pela garra, esse agente deve enviar um sinal de conclusão ao ECL para que ela se mova para outra posição alvo. É permitido a garra realizar 11 tipos diferentes de ações discretas:

•	Abrir a garra;
•	Fechar a garra;
•	Sinalizar preenchimento de fileira à esteira da caixa de latas; 
•	Movimentar para as 8 posições descritas na figura 16 da imagem abaixo, podendo se deslocar de qualquer posição para a outra.

<p align="center"><img src="Images/handling_positions.png"></p>

Por sua vez, o sistema recebe informações de estado de 6 variáveis: 
•	Sensor de fim de curso da esteira da caixa de lata (variável discreta);
•	Sensor de presença de lata na garra (variável discreta);
•	Posição da garra no eixo Y (variável contínua);
•	Posição da garra no eixo X (variável contínua);
•	Sensor de fim de curso da garra, indicando se está fechada ou aberta (variável discreta);
•	Sinal enviado pela esteira da caixa de lata, indicando que se ela está em movimento ou não está sobre o sensor de fim de curso da posição da garra (variável discreta).

# Para treinamento da garra manipualdora de latas:

## Abra o Jupyter Notebook:

Se você instalou o Anaconda, abra o Anaconda Navigator e clique no botão "Launch" para o Jupyter Notebook.<br>
Se você instalou o Python e o Jupyter Notebook usando o pip, abra o terminal ou prompt de comando e digite o comando "python -m notebook".<br>
No Linux ou macOS, abra o terminal e digite o comando "python -m notebook".<br>

Independentemente do método escolhido, após o Jupyter Notebook ser iniciado, ele abrirá uma página da web no seu navegador padrão com o endereço "http://localhost:8888/tree". A partir daí, você pode criar um novo notebook ou abrir um já existente.

## Ative o servidor websocket:

Todos os processos de treino e teste requerem ativação do servidor websocket para gestão de comunicação entre agente (cliente) e ambiente (servidor).Para isto siga os passos seguintes:

### 1- Abra o notebook Socket Communication:

Executar o ficheiro no diretório DigitalTwinRL/Socket/Socket Communication.ipynb 

### 2- Execute o servidor websocket:

Basta correr a primeira célula do notebook e o ficheiro python irá ativar conexão TCP/IP local, porta 12000. Caso já esteja ativo e a célula for executada novamente, a conexão será desativada. Em todo treinamento ou teste deve-se certificar que a conexão esteja ativa.

## Gerar o ambiente de treinamento da garra manipualdora de latas:

### 1- Abra o notebook Handling enviroment:

Executar o ficheiro no diretório DigitalTwinRL/Enviroment/Handling_enviroment.ipynb

### 2- Prepare o ambiente de treinamento da garra manipualdora de latas:

Execute as células abaixo de criação do ambiente:

1 - Importa bibliotecas;
2 - Cria funções de encoding/decoding em json;
3 - Define função do ambiente de treino.

### 3- Verifique a conexão websocket:

Execute a célula 4 "Verifica se o servidor socket está ativo" para checar se o servidor está ativo. Caso não esteja, verifique o notebook Socket Communication.ipynb nos passos anteriores.

### 4- Ative o ambiente da garra manipualdora de latas:

Execute a célula 5 "Ativa o ambiente para treino". A célula ficará permanentemente a correr, aguardando comandos do agente. Um log ações é exebido abaixo da célula durante o trnamento do agente.

## Gerar o ambiente de treinamento da garra manipualdora de latas:













