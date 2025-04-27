# Projeto: Monitoramento de Luminosidade - Vinheria Agnello

## 📋 Descrição
Sistema de monitoramento de luminosidade desenvolvido para a Vinheria Agnello, utilizando Arduino, LEDs, buzzer, display LCD e sensor LDR (fotoresistor).  
O projeto sinaliza quando a luminosidade ambiente está adequada, em alerta ou crítica para a conservação dos vinhos.

---

## 🛠 Materiais Utilizados
- Arduino Uno
- Sensor de luz LDR (fotoresistor)
- Display LCD 16x2
- Potenciômetro (para ajuste do contraste do LCD)
- LEDs: verde, amarelo e vermelho
- Buzzer passivo
- Protoboard
- Cabos jumpers
- Resistores (para os LEDs)
- Resistor (para o LDR)

---

## ⚡ Funcionamento
- O sensor LDR lê a quantidade de luz no ambiente.
- A leitura é convertida para porcentagem usando a função `map()`.
- O sistema calcula a média de 10 leituras para maior precisão.
- Dependendo da luminosidade:
  - **LED verde** acende para luminosidade adequada (≤30%).
  - **LED amarelo** acende e **buzzer toca por 3 segundos** para luminosidade de alerta (31% a 70%).
  - **LED vermelho** acende para luminosidade alta (>70%).
- O LCD exibe:
  - Primeira linha: "Vinheria Agnello"
  - Segunda linha: "Luz: XX%"

---

## 🖥 Como Usar
1. Monte o circuito conforme o esquema eletrônico.
2. Faça o upload do código para o Arduino usando a IDE Arduino.
3. Observe no LCD e nos LEDs o comportamento baseado na luminosidade ambiente.

---

## 📌 Observações
- O buzzer usado é do tipo passivo, por isso foi necessário utilizar a função `tone()`.
- Foi utilizada média de leituras para garantir maior estabilidade nas medições.
- A calibração dos valores mínimos e máximos de luminosidade foi ajustada para a simulação.

---

## 👥 Integrantes do Grupo
- Henrique Keigo Nakashima Minowa - RM: 564091
- Eduardo Delorenzo Moraes - RM: 561749
- Matheus Bispo Faria Barbosa - RM: 562140
