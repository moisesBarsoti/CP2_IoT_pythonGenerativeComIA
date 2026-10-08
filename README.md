# 🏠 SmartHome

**Checkpoint 02 - Disruptive Architectures: IoT, IoB & Generative AI**

Projeto desenvolvido para a disciplina de Disruptive Architectures do curso de Análise e Desenvolvimento de Sistemas da FIAP.

## 👨‍💻 Desenvolvedor

- **Nome:** Moisés Barsoti Andrade de Oliveira
- **RM:** 565049
- **Turma:** 2TDSPO

## 📑 Índice

1. [Sobre o Projeto](#-sobre-o-projeto)
2. [Objetivos](#-objetivos)
3. [Tecnologias Utilizadas](#-tecnologias-utilizadas)
4. [System Prompt](#-system-prompt)
5. [Funcionalidades Desenvolvidas](#-funcionalidades-desenvolvidas)

## 📌 Sobre o Projeto

O **SmartHome AI** é um assistente virtual especializado em casas inteligentes e automação residencial, desenvolvido com Python e modelos de inteligência artificial generativa.

O projeto busca auxiliar usuários com dúvidas relacionadas à Internet das Coisas (IoT), sensores inteligentes, dispositivos conectados, economia de energia e segurança residencial.

A aplicação utiliza a API Google Gemini para gerar respostas e possui integração preparada para Hugging Face.

Além do chatbot, o projeto implementa controle de temperatura, guardrails, gerenciamento do histórico de conversas, interface web e uma API REST com sessões independentes.

## 🎯 Objetivos

- Desenvolver um assistente especializado em automação residencial.
- Implementar guardrails para restringir respostas fora do tema.
- Investigar a influência da temperatura na geração de respostas.
- Implementar memória de conversação.
- Disponibilizar seleção entre modelos de inteligência artificial.
- Desenvolver uma interface web utilizando Gradio.
- Implementar uma API REST com históricos independentes.

## 🛠 Tecnologias Utilizadas

| Tecnologia | Utilização |
|---|---|
| Python | Linguagem principal |
| Google Colab | Ambiente de desenvolvimento |
| Google Gemini API | Geração de respostas |
| Hugging Face Inference API | Integração com modelo Llama |
| Gradio | Interface web interativa |
| FastAPI | Desenvolvimento da API REST |
| Uvicorn | Servidor da API |
| Requests | Testes HTTP |
| GitHub | Versionamento e entrega |

## 🧠 System Prompt

O assistente foi configurado para atuar exclusivamente no contexto de casas inteligentes e automação residencial.

O prompt estabelece que a IA deve responder perguntas sobre sensores, dispositivos inteligentes, assistentes virtuais, conectividade e segurança residencial.

### Principais regras

- Responder sempre em português brasileiro.
- Utilizar linguagem clara, objetiva e acessível.
- Limitar as respostas a cinco frases.
- Fornecer orientações simples quando necessário.
- Evitar informações técnicas inventadas.
- Não fornecer instruções que comprometam a segurança dos usuários.
- Recusar educadamente assuntos fora do escopo.

Essas regras permitem controlar o comportamento do assistente e manter suas respostas relacionadas ao tema estabelecido.

## ⚙️ Funcionalidades Desenvolvidas

### Etapa 1 - Guardrails

Foram implementadas três versões de system prompt:

1. **Sem restrição:** o assistente pode responder perguntas sobre qualquer assunto.
2. **Com restrição de tema:** o assistente responde exclusivamente perguntas relacionadas a casas inteligentes.
3. **Com restrição de tema e formato:** o assistente restringe o conteúdo e responde em até três frases, sem listas.

**Resultado:** o Gemini respondeu às perguntas sobre automação residencial e recusou educadamente perguntas fora do escopo quando os guardrails foram aplicados.

### Etapa 2 - Controle de Temperatura

Foram realizados testes utilizando:

- `temperature=0.0` — geração com menor aleatoriedade.
- `temperature=1.0` — geração com maior aleatoriedade.

As perguntas abordaram sensores residenciais e segurança de câmeras conectadas.

**Resultado:** as respostas sobre sensores foram praticamente idênticas nas duas temperaturas. Já as respostas sobre câmeras apresentaram diferenças nas recomendações de segurança, incluindo WPA2/WPA3, VPN e UPnP.

Os testes demonstraram que temperaturas maiores podem produzir respostas diferentes
