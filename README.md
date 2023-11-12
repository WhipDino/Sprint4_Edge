# Projeto de Monitoramento de Ambiente com Arduino e IoT

Este projeto demonstra como criar um sistema de monitoramento de ambiente utilizando um Arduino, sensores ultrassônicos, um LDR (Light-Dependent Resistor), um display LCD, e IoT (Internet das Coisas) para visualizar e analisar os dados coletados em tempo real.

# Sensores nos postes

O foco do nosso projeto é diminuir o consumo de energia e a poluição visual causada pelos postes de luz. Utilizaremos luz baixa enquanto ninguém estiver próximo, assim que for detectada a presença de um pedestre ou carro, os postes atingirão o nível de luminosidade necessário para a locomoção naquele trecho. Dessa forma é possível usar as tecnologias estudadas no curso para contribuir com a ideia de cidades inteligentes e sustentabilidade. Com os dados coletados pelos sensores de movimento, seremos capazes de entender o fluxo de pessoas e automóveis em cada local onde a tecnologia for utilizada, com essas informações é possível reduzir os tráfego em certas regiões e ajudar aplicativos de GPS a traçarem melhores rotas.


## Visão Geral

A Internet das Coisas (IoT) permite a conexão de dispositivos do mundo físico à internet, possibilitando o monitoramento e controle remoto de diversos parâmetros. Neste projeto, utilizamos um Arduino para coletar dados de um sensor ultrassônico e um LDR, que medem distância e luminosidade, respectivamente. Esses dados são transmitidos para um servidor Node-RED via MQTT (Message Queuing Telemetry Transport) e, em seguida, enviados para a plataforma TagoIO para análise e visualização.

## Componentes

- Ultrassônico
- LDR
- Potenciômetro
- Display LCD
- LED
- Resistor

### Hardware

- Arduino Uno
- Sensor Ultrassônico HC-SR04
- LDR (Light-Dependent Resistor)
- Display LCD 16x2
- Fonte de Tensão
- Jumpers e cabos diversos

### Software

- [Arduino IDE](https://www.arduino.cc/en/software)
- [Node-RED](https://nodered.org/)
- [TagoIO](https://tago.io/)

## Configuração

1. **Montagem do Hardware:** Monte os componentes conforme o esquema de ligação fornecido (inserir esquema aqui).

2. **Programação do Arduino:** Carregue o código do Arduino disponível neste repositório para o seu Arduino utilizando a Arduino IDE.

3. **Node-RED:** Configure um fluxo no Node-RED para receber dados do Arduino via MQTT. Certifique-se de ajustar as configurações MQTT de acordo com a sua rede.

4. **TagoIO:** Crie uma conta no TagoIO e configure uma integração MQTT para receber os dados do Node-RED.

5. **Dashboard TagoIO:** Crie um dashboard personalizado no TagoIO para visualizar os dados coletados em tempo real.

## Uso

Após a configuração, o sistema estará coletando dados do sensor ultrassônico e do LDR. Esses dados serão enviados para o Node-RED e, em seguida, para o TagoIO. Você pode visualizar e analisar esses dados através do seu dashboard personalizado no TagoIO.
- Token de acesso: c4b8e693-5672-4303-bdae-52ce965afad4



![image](https://github.com/WhipDino/Sprint3_Edge/assets/95549158/78764c4c-b83f-4228-b49e-0187f2a331b6)



## Integração

Neste projeto, realizamos uma integração eficaz entre o Arduino, o Node-RED e a plataforma TagoIO para coleta, processamento e visualização de dados em tempo real.

### Conexão Arduino e Node-RED

1. **Hardware:** Configuramos um Arduino Uno para coletar dados de sensores, incluindo um sensor ultrassônico HC-SR04 e um LDR (Light-Dependent Resistor). A conexão física entre os sensores e o Arduino foi estabelecida de acordo com o esquema de ligação apropriado.

2. **Programação do Arduino:** Desenvolvemos o código do Arduino utilizando a Arduino IDE. O código foi projetado para ler os dados dos sensores e transmiti-los para o Node-RED através do protocolo MQTT.

3. **Node-RED:** No Node-RED, configuramos um fluxo para receber os dados do Arduino via MQTT. Utilizamos o Node-RED para processar os dados, realizar a lógica desejada e, em seguida, transmiti-los para a plataforma TagoIO.

[![Watch the video (https://i.stack.imgur.com/Vp2cE.png)](https://www.youtube.com/watch?v=4R-H2aaJFMI)


![image](https://github.com/WhipDino/Sprint3_Edge/assets/95549158/2869481a-747d-40d6-86a6-465c318f6d82)

### Conexão Node-RED e TagoIO

1. **TagoIO:** Criamos uma conta no TagoIO e configuramos um _Device_ para representar o Arduino em nossa aplicação. Em seguida, configuramos uma integração MQTT no TagoIO para receber os dados do Node-RED.

2. **Node-RED para TagoIO:** No Node-RED, usamos um nó MQTT para enviar os dados coletados para o TagoIO. Certificamo-nos de configurar corretamente o endereço do servidor MQTT do TagoIO e as credenciais de segurança necessárias.

![image](https://github.com/WhipDino/Sprint3_Edge/assets/95549158/6be54f28-f21c-4bb3-9c70-e03a157263b1)


### Dashboard Personalizado

No TagoIO, criamos um dashboard personalizado para visualizar os dados coletados em tempo real. Utilizamos widgets personalizados para exibir informações relevantes, como distância medida pelo sensor ultrassônico e níveis de luminosidade detectados pelo LDR.

Essa integração entre o Arduino, Node-RED e TagoIO permite o monitoramento e análise contínuos de dados de sensores em tempo real, fornecendo informações valiosas sobre o ambiente monitorado.

![image](https://github.com/WhipDino/Sprint3_Edge/assets/95549158/644ccc2e-598c-4331-845e-617c407d3417)
