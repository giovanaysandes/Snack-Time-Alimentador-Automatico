# Snack-Time-Alimentador-Automatico

Snack Time é um projeto que visa construir um alimentador automatico para pets. Além de liberar a ração ao clicar em um botão, também possibilita receber uma mensagem pelo whatsapp de quando o animal estiver comendo, por meio de um sensor de movimento.

<h2> Os materiais utilizado para a criação do projeto foram  </h2>
- Arduino UNO <br>
- Sensor de movimento PIR -- Responsável por capturar o movimento do animal quando está se alimentando <br>
- Servo Motor MG 996R - Responsável por realizar o giro e permitir a saída do alimento <br>
- Botão <br>
- Led <br>
- 2 latas, sendo um com o diametro maior que a outra <br>

<h2> Instalações Necessárias: </h2>
Noje js  <br>
Node Red  <br>
Arduino IDE  <br>

<h2> Extensões Necessárias: </h2>
Arduino IDE - Biblioteca Firmata <br>
Node red - Para utilizar as portas de entradas e saída do arduino foi necessário instalar a extensão. <br>
 
![image](https://user-images.githubusercontent.com/80367383/202944656-ba3bf1e3-0aab-4f54-8409-ddfaca2cc549.png) <br>

Para utilizar o Broker na plataforma do node-red <br>
 
![image](https://user-images.githubusercontent.com/80367383/202944670-9402a530-b8b8-4ef1-a9d3-3be97bb92bb8.png)<br>

E para que o protocolo MQTT envie uma notificação para o WPP foi instalada a extensão <br>
  
![image](https://user-images.githubusercontent.com/80367383/202944678-fd0339bc-1430-4bb3-a8f9-5857bfaf4de7.png) 


<h2> Programação: </h2>
Neste repositório encontra-se :  <br>
- Os arquivos necessários para fazer conexão do arduino para o node-red, por meio da biblioteca firmata na própria IDE do Arduino.  <br>
- Código Node-red para realizar a conexão com o protocolo MQTT, acionamento do sensor e servo motor 


<h2> Montagem : </h2>
1. Realize um corte no centro das latas e 1/4  <br>
 
![image](https://user-images.githubusercontent.com/80367383/202943959-8ff85dc4-b2f9-4245-83f3-5753bc72e07c.png) <br>

A parte da helice do motor deve estar presa em uma das latas, enquanto o seu corpo em outra parte, permitindo assim a saída do alimento atravez do buraco. <br>

<h2> Modelo de Montagem </h2>
![image](https://user-images.githubusercontent.com/80367383/202945491-f581b12a-69d8-4a56-8f26-152ad8350642.png)<br>
Neste modelo de montagem temos o sensor de movimento PIR que será acionado quando animal estiver próximo de seu comedouro, ao ser ativado irá transmitir uma mensagem (“nome do animal está comendo”) para o aplicativo de texto whatsapp, por meio do protocolo MQTT e irá acender um led. Além disso, por meio do botão o MG996 servo motor será ativado e realizará um giro de acordo com o tempo de aperto no botão, ao realizar esse giro os dois buracos feitos nas latas irão se encontrar e o alimento irá ultrapassar entre eles para o comedouro do animal, dessa forma será liberado uma porção de ração.
