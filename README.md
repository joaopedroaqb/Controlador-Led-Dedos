# Controlador de LED com Visão Computacional

Este é um script Python que utiliza visão computacional para controlar LEDs com base no movimento dos dedos das mãos. O código utiliza a biblioteca OpenCV para capturar frames da câmera e a biblioteca `cvzone` para detecção e rastreamento de mãos. Além disso, é necessário o módulo `pyfirmata` para comunicação com uma placa Arduino, que controla os LEDs.

## Pré-requisitos

- Python 3.x
- OpenCV
- [cvzone](https://github.com/cvzone/cvzone)
- [pyfirmata](https://github.com/tino/pyFirmata)
- Arduino configurado para receber comandos via Firmata

## Como usar

1. **Instale as dependências:**

   ```bash
   pip install opencv-python
   pip install cvzone
   pip install pyfirmata

Conecte seu Arduino e ajuste a porta na linha board = Arduino('COM1') para a porta correta.
A porta vai estar definido de acordo com seu computador, para descobrir qual a porta correta, pode acessar sua IDE que está usando o arduino.

Uma janela de vídeo será aberta, mostrando o feed da câmera. A os leds irá ligar de acordo com a quantidade de dedos levantados.

## Descrição
Este controlador de LED utiliza a detecção de mãos para identificar os movimentos dos dedos. Quando um ou mais dedos são detectados, os LEDs correspondentes são acesos de acordo com a quantidade de dedos levantados. Cada LED representa um dedo, e a intensidade luminosa varia de 1 a 5, dependendo do número de dedos levantados.

Observação: Pressione 'q' para fechar a janela de vídeo e encerrar o programa.

Este script é uma demonstração simples de interação entre visão computacional e hardware para controlar LEDs com gestos de mão. Experimente e adapte conforme necessário para atender aos seus requisitos específicos.
