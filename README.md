# Imersão AI _ Alura com o Google Gemini


# 🌍 Sistema de Informações de Viagem Inteligente

Este projeto utiliza o modelo de linguagem Gemini do Google e o Agent Development Kit (ADK) para criar um sistema inteligente de informações de viagem. Ao fornecer um destino, o sistema consulta a web em tempo real, planeja informações úteis, gera um resumo informativo e revisa o conteúdo para o usuário.

## 🚀 Funcionalidades

1.  **Busca Inteligente de Novidades (Agente 1):**
    * Utiliza a ferramenta de busca do Google para encontrar as notícias, eventos e lançamentos mais recentes relacionados ao destino de viagem especificado.
    * Prioriza informações recentes e relevantes para viajantes (máximo de um mês).
    * Foca em eventos culturais, novidades turísticas, atualizações de transporte e informações úteis.

2.  **Planejamento de Informações de Viagem (Agente 2):**
    * Analisa os tópicos encontrados pelo Agente 1.
    * Aprofunda as informações práticas e inspiradoras sobre cada tópico usando a busca do Google.
    * Gera resumos concisos e úteis para o usuário, destacando pontos principais, detalhes relevantes e sugestões de como aproveitar a informação na viagem.
    * Seleciona o tema mais relevante e útil, justificando a escolha e apresentando um breve plano de informações (título, principais detalhes, recomendações).

3.  **Geração de Resumo Informativo (Agente 3):**
    * Cria um resumo conciso e útil para viajantes interessados no destino.
    * Inclui informações essenciais como moeda local, clima típico/melhor época para visitar, idioma oficial e necessidade de visto.
    * Baseia-se no plano de informações detalhado gerado pelo Agente 2.

4.  **Revisão e Consolidação das Informações (Agente 4):**
    * Revisa o rascunho gerado pelo Agente 3.
    * Consolida as informações de forma sucinta e clara para o usuário final, garantindo que não faltem detalhes importantes para o planejamento da viagem.

## ⚙️ Tecnologias Utilizadas

* **Google Gemini:** Modelo de linguagem multimodal do Google para geração de texto e compreensão.
* **Google Agent Development Kit (ADK):** Framework para construir agentes inteligentes e colaborativos.
* **Python:** Linguagem de programação principal.
* **`google-genai`:** Biblioteca Python para interagir com a API do Google Gemini.
* **`google-adk`:** Biblioteca Python do Agent Development Kit.
* **Google Search Tool:** Ferramenta do ADK para realizar buscas na web.
* **IPython.display:** Para exibir Markdown e HTML no ambiente Colab.
* **`python-dotenv` (Opcional):** Para gerenciar chaves de API de forma segura (não utilizado diretamente no código, mas recomendado para produção).

## 🛠️ Pré-requisitos

* Uma conta Google Cloud com acesso à API Gemini.
* Uma chave de API do Google Gemini configurada como um segredo do usuário no Google Colab (ou configurada como uma variável de ambiente).
* Ambiente Python com as bibliotecas listadas em "Tecnologias Utilizadas" instaladas.

## 🚀 Como Executar

1.  **Configurar a API Key:**
    * No Google Colab, vá em "Ferramentas" -> "Segredos".
    * Crie um novo segredo com o nome `GOOGLE_API_KEY` e cole sua chave de API do Google Gemini.

2.  **Instalar as Bibliotecas:**
    * Execute a primeira célula do notebook (`%pip -q install google-genai`).
    * Execute a célula para instalar o ADK (`!pip install -q google-adk`).

3.  **Executar o Código:**
    * Execute as células de código sequencialmente.
    * Quando solicitado, digite o destino de viagem para o qual você deseja obter informações.

4.  **Visualizar os Resultados:**
    * O sistema exibirá os resultados de cada agente, desde a busca inicial até o resumo final da viagem, formatados em Markdown.

## 💡 Uso

Ao executar o script, você será solicitado a inserir um destino de viagem. O sistema então processará sua solicitação através dos quatro agentes, fornecendo informações atualizadas e relevantes para o seu planejamento diretamente na tela.
