# A4-Objetos-inteligentes-conectados

# 🌱 IoT para Monitoramento de Umidade do Solo e Condições Ambientais na Agricultura

Este projeto apresenta uma solução de **Agricultura de Precisão** utilizando **Internet das Coisas (IoT)**, com o objetivo de monitorar em tempo real a umidade do solo e as condições climáticas, promovendo o uso eficiente da água e a automação da irrigação.

## 👨‍🔬 Autores

- Mateus Takashi Kochi  
- Lucas Alves da Silva  
- Lucas Fernandes Batista  
- Universidade Presbiteriana Mackenzie

## 🎯 Objetivos

- Automatizar a irrigação com base em dados ambientais;
- Otimizar o uso da água e dos recursos naturais;
- Aumentar a produtividade e sustentabilidade da produção agrícola.

---

## 🧰 Tecnologias e Componentes Utilizados

| Componente                    | Descrição                                                 |
|------------------------------|-----------------------------------------------------------|
| NodeMCU ESP8266              | Microcontrolador com conectividade Wi-Fi integrada        |
| Sensor de Umidade do Solo    | FC-28 (simulado com potenciômetro no Wokwi)              |
| Sensor de Temperatura/Umidade| DHT22                                                     |
| Atuador                      | Válvula solenoide (simulada com LED no Wokwi)            |
| IDE                          | Arduino IDE                                               |
| Protocolo de Comunicação     | MQTT (via biblioteca PubSubClient)                       |
| Simulador                    | [Wokwi](https://wokwi.com)                               |

---

## 🔗 Acesse a Simulação no Wokwi

👉 [Clique aqui para abrir a simulação](https://wokwi.com/projects/397826075247285249)

---

## ⚙️ Funcionamento do Sistema

1. **Leitura dos Sensores:**
   - O sensor DHT22 mede a **temperatura** e **umidade do ar**.
   - O potenciômetro simula a **umidade do solo** do sensor FC-28.

2. **Processamento dos Dados:**
   - O NodeMCU lê os dados e verifica se a umidade do solo está abaixo de um limiar (ex: `< 30%`).

3. **Controle da Irrigação:**
   - Se a umidade do solo estiver baixa, um **LED é acionado** simulando a abertura da **válvula solenoide** para irrigação.
   - Caso contrário, o LED permanece desligado.

4. **Comunicação via MQTT (opcional):**
   - Os dados podem ser enviados a um **broker MQTT** como o Mosquitto.
   - Ideal para dashboards e tomada de decisão remota.

---

