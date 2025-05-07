# Plantinhas - Documentação

<div align="center">
  <img src="assets/plantinhas-ico.png" alt="Plantinhas Logo" width="200">
</div>

## 🌱 Visão Geral

Plantinhas é um jardim virtual onde os usuários podem acompanhar o crescimento de suas plantas favoritas e comparar o progresso com outros jardineiros. É o lugar perfeito para descobrir se a grama do vizinho realmente é mais verde!

## 🏗️ Arquitetura

O projeto é composto por vários componentes independentes:

- 🖌️ **Frontend**: Next.js + Tailwind CSS
- 🔧 **Backend**: Django com Django Rest Framework
- 🤖 **AI Generation API**: FastAPI integrado com OpenAI
- 🌦️ **APIs de Clima e Tempo**: Integração com serviços externos

> ⚠️ **Nota**: Os componentes do sistema estão em outros repositórios. Este repositório contém apenas documentação.

## 🔄 Fluxo Principal

1. Usuário cria uma conta e configura seu perfil
2. Adiciona plantas ao seu jardim virtual
3. Acompanha o crescimento através de tarefas e notificações
4. Compartilha o progresso no fórum e feed social
5. Recebe recomendações personalizadas baseadas em IA

## 📲 Principais Funcionalidades

- 🌿 **Gerenciamento de Plantas**: Cadastro e monitoramento de plantas
- 📝 **Fórum de Discussão**: Compartilhamento de experiências e dúvidas
- 📊 **Acompanhamento de Crescimento**: Registro do desenvolvimento das plantas
- 🤖 **Recomendações por IA**: Sugestões personalizadas para cultivo
- 🌦️ **Integração Climática**: Alertas baseados em condições meteorológicas

## 🧪 Mockoon

Para desenvolvimento local, utilizamos o Mockoon para simular as APIs. Confira a configuração em [`mockoon/mockoon.json`](mockoon/mockoon.json).

## 🗂️ Modelo de Dados

Um diagrama ER detalhado do sistema pode ser encontrado em [`diagrama-er/README.md`](diagrama-er/README.md).

---

📝 *Esta documentação é específica para este repositório de documentação. Os componentes do sistema estão em repositórios separados.*
