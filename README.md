# monitor-cardiaco-IoT
Meu projeto IoT da Universidade Presbiteriana Mackenzie. O projeto foi desenvolvido em C++ utilizando a IDE Arduino.

## <br> Dados obtidos via MQTT no Ubidots

Gráfico de Leitura no Ubidots: No contexto do projeto de monitoramento de ECG utilizando o ESP32 e o sensor AD8232, implementei um filtro de média móvel para suavizar os sinais de entrada do sensor. O filtro de média móvel é uma técnica fundamental no processamento de sinais para reduzir o ruído aleatório e melhorar a confiabilidade dos dados medidos. Esta implementação especificamente utiliza uma média móvel simples, onde o valor atual do sensor é combinado com o último valor filtrado. O fator de 0.5 para ambos os valores atuais e anteriores equilibra a contribuição de cada um, oferecendo uma suavização efetiva sem atrasar demais a resposta a mudanças reais no sinal.

![Captura de tela 2024-05-10 201025](https://github.com/pedrojhenrique/monitor-cardiaco-IoT/assets/105826347/5d0239a5-b290-4bb5-ab1c-b38bcca7592d)
