# monitor-cardiaco-IoT
Meu projeto IoT da Universidade Presbiteriana Mackenzie. O projeto foi desenvolvido em C++ utilizando a IDE Arduino.

## <br> Funcionamento

Bateria: Uma fonte de 3.7V, como uma bateria LiPo, é adequada para o protótipo, 
oferecendo tensão necessária para o funcionamento do ESP32 e do sensor ECG 
AD8232.
Sensor ECG AD8232: Captura os sinais elétricos do coração e envia para o ESP32.
ESP32: Processa os dados do sensor ECG e verifica se há alguma anomalia nos 
batimentos cardíacos. Se algo atípico for detectado, o ESP32 ativa o buzzer.
Buzzer: Atua como um alerta sonoro em caso de detecção de anomalias cardíacas.
Comunicação MQTT: Configuração do ESP32 para enviar dados dos batimentos 
cardíacos via protocolo MQTT para um servidor ou plataforma na nuvem, 
permitindo monitoramento remoto.

## <br> 2.8.	Modelo de Montagem 

O sensor ECG AD8232 é conectado ao microcontrolador ESP32, que irá processar os dados dos batimentos cardíacos. O ESP32 está ligado a um buzzer, que será utilizado para alertar o usuário em caso de detecção de anomalias cardíacas. Os cabos de alimentação do sensor ECG são conectados às entradas de 3,3V e GND do ESP32, enquanto o sinal de saída do sensor é conectado a um dos pinos analógicos. O buzzer é conectado a um pino digital do ESP32 e a GND. Este sistema é alimentado por uma fonte de 3,7V, adequada para a operação dos componentes eletrônicos envolvidos. Também há a possibilidade de alimentar todo o circuito através de um cabo USB direto de um computador, já que a ESP32 possui entrada para tal.

## <br> Dados obtidos via MQTT no Ubidots

Gráfico de Leitura no Ubidots: No contexto do projeto de monitoramento de ECG utilizando o ESP32 e o sensor AD8232, implementei um filtro de média móvel para suavizar os sinais de entrada do sensor. O filtro de média móvel é uma técnica fundamental no processamento de sinais para reduzir o ruído aleatório e melhorar a confiabilidade dos dados medidos. Esta implementação especificamente utiliza uma média móvel simples, onde o valor atual do sensor é combinado com o último valor filtrado. O fator de 0.5 para ambos os valores atuais e anteriores equilibra a contribuição de cada um, oferecendo uma suavização efetiva sem atrasar demais a resposta a mudanças reais no sinal.

![Captura de tela 2024-05-10 201025](https://github.com/pedrojhenrique/monitor-cardiaco-IoT/assets/105826347/5d0239a5-b290-4bb5-ab1c-b38bcca7592d)
