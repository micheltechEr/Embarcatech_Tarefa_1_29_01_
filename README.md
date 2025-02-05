# Controle de Semáforo com Temporizadores - Raspberry Pi Pico

## Descrição do Projeto
Este projeto foi desenvolvido para praticar o uso de **temporizadores** conforme ensinado na aula. A atividade consiste em implementar um **semáforo controlado por temporizadores**, alternando entre os estados de LED vermelho, amarelo e verde em intervalos regulares de 3 segundos.

O código utiliza a biblioteca `pico/stdlib.h` para configurar os pinos GPIO e gerenciar o temporizador repetitivo (`repeating_timer`). Além disso, o programa exibe no console o tempo decorrido em segundos, permitindo acompanhar a execução.

---

## Componentes Utilizados
- **LED Vermelho (Pino 11):** Representa o estado "pare" do semáforo.
- **LED Amarelo (Pino 12):** Representa o estado de transição ("atenção").
- **LED Verde (Pino 13):** Representa o estado "siga".
- **Raspberry Pi Pico:** Placa utilizada para executar o código.
- **Resistores:** Para limitar a corrente nos LEDs (recomenda-se 220Ω ou 330Ω).

---

## Funcionalidades do Projeto
- **Controle de LEDs via temporizador:**
  - O semáforo alterna entre os estados (vermelho → amarelo → verde → vermelho) a cada 3 segundos.
- **Exibição do tempo decorrido:**
  - O programa imprime no console o tempo decorrido em segundos, incrementando o contador a cada segundo.
- **Uso de temporizadores:**
  - Implementação de um temporizador repetitivo (`repeating_timer`) para controlar as transições de estado.

---

## Guia de Funcionamento na Sua Máquina

Para executar este projeto localmente, siga as instruções abaixo:

### 1. **Clone o repositório:**
   - Abra o **VS Code** e clone este repositório para sua máquina.

### 2. **Importe o projeto:**
   - Certifique-se de ter as extensões do **Raspberry Pi Pico** instaladas no VS Code.
   - Importe o projeto para poder compilá-lo e executá-lo na placa RP2040.

### 3. **Conecte a placa:**
   - Conecte a placa ao computador via USB e coloque-a no modo **BOOTSEL**.

### 4. **Compile o código:**
   - Compile o código diretamente no VS Code.

### 5. **Simulação no Wokwi:**
   - Para simular o projeto, abra o arquivo `diagram.json` disponível nos arquivos do projeto e execute-o no [Wokwi](https://wokwi.com).

### 6. **Execute na placa:**
   - Após a compilação e com a placa no modo **BOOTSEL**, clique em **Executar** ou **Run** para carregar o programa na placa.

---

## Funcionamento do Semáforo

O semáforo funciona da seguinte forma:
1. **Estado Inicial:**
   - O LED vermelho é aceso, indicando o estado "pare".

2. **Transição de Estados:**
   - Após 3 segundos, o LED vermelho é desligado e o LED amarelo é aceso, indicando o estado "atenção".
   - Após mais 3 segundos, o LED amarelo é desligado e o LED verde é aceso, indicando o estado "siga".
   - Após outros 3 segundos, o ciclo retorna ao estado inicial (LED vermelho aceso).

3. **Exibição no Console:**
   - O programa imprime no console o tempo decorrido em segundos, permitindo acompanhar a execução.

---

## Código Fonte

O código fonte está organizado da seguinte forma:
- **Função `repeating_timer_callback`:** Controla as transições de estado do semáforo.
- **Função `setup`:** Configura os pinos GPIO e inicializa o temporizador repetitivo.
- **Loop Principal (`main`):** Exibe o tempo decorrido no console.

---

## Observações Finais

Este projeto foi desenvolvido com foco em boas práticas de programação, organização e documentação. Ele é ideal para estudantes que desejam praticar o uso de temporizadores e GPIOs no Raspberry Pi Pico.

Caso tenha dúvidas ou sugestões, sinta-se à vontade para abrir uma **issue** ou entrar em contato.

---

### Créditos
- **Autor:** Ângelo Miguel Ribeiro Cerqueira Lima
- **Data:** 03/02/2024

---