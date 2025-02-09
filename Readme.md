# Controle de Servo Motor com RP2040

## Descrição

Este projeto controla um servo motor utilizando a Raspberry Pi Pico e o microcontrolador RP2040. O programa configura o PWM para operar a 50 Hz e movimenta o servo de 0 a 180 graus e de volta para 0 graus continuamente.

O desenvolvimento FOI feito no **Visual Studio Code** vinculado ao **Wokwi**, um simulador online para microcontroladores.

## Requisitos

- **Hardware:**

  - Raspberry Pi Pico
  - Servo motor compatível com PWM

- **Software:**

  - Visual Studio Code
  - Extensão C/C++
  - SDK do Raspberry Pi Pico
  - Wokwi (para simulação)

## Configuração do PWM

- Frequência: **50 Hz** (período de 20ms)
- Wrap: **25000**
- Divisor de clock: **100**
- Pino do servo motor: **GPIO 22**

## Como Rodar o Projeto

1. **Abra o VS Code e carregue o projeto.**
2. **Execute a compilação** do código.
3. **Se estiver no Wokwi**, execute a simulação normalmente.
4. **O servo se movimentará continuamente** entre 0 e 180 graus com movimentos suaves.

## Comportamento do Programa

1. **Inicializa o PWM no pino GPIO 22.**
2. **Define três posições fixas iniciais:**
   - 180 graus (duty cycle: **12%** ou **3000/25000**)
   - 90 graus (duty cycle: **7.35%** ou **1838/25000**)
   - 0 graus (duty cycle: **2.5%** ou **625/25000**)
3. **Movimenta continuamente o servo** de 0 a 180 graus e depois volta para 0 graus com incrementos suaves de **5 µs** e pausas de **10ms**.

## Conexão do Hardware

| Pino da Pico      | Servo Motor |
| ----------------- | ----------- |
| GPIO 22           | Sinal (PWM) |
| VBUS (5V) ou VSYS | VCC         |
| GND               | GND         |



