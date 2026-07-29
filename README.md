# FM Broadcast Monitor

Sistema experimental para transmissão, recepção e análise de sinais FM, combinando telecomunicações, processamento digital de sinais e áudio.

## Objetivo

Desenvolver uma ferramenta capaz de:

- Simular a transmissão e recepção de sinais FM;
- Demodular e recuperar o áudio transmitido;
- Visualizar os espectros do sinal FM e do áudio;
- Avaliar a influência do ruído no canal;
- Futuramente receber transmissões reais utilizando RTL-SDR;
- Implementar métricas de qualidade do sinal e do áudio.

## Estado atual

A primeira versão simulada foi implementada no GNU Radio Companion.

O sistema atualmente:

- Gera um tom de áudio de 1 kHz;
- Modula o áudio utilizando WBFM;
- Simula um canal de comunicação com ruído ajustável;
- Demodula o sinal FM;
- Exibe o espectro do sinal transmitido;
- Exibe o espectro e a forma de onda do áudio recuperado;
- Reproduz o áudio recuperado.

## Arquitetura

```text
Signal Source
      ↓
WBFM Transmit
      ↓
Throttle
      ↓
Channel Model
      ↓
WBFM Receive
      ↓
Audio Analysis and Playback
