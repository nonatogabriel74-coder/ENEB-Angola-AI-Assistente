# 🏗️ Arquitetura do Sistema - ENEB Angola AI Assistant

## 🎯 Visão Geral
O **ENEB Angola AI Assistant** é uma solução baseada em **Retrieval-Augmented Generation (RAG)** e Engenharia de Prompts projetada para fornecer atendimento, triagem de candidatos e orientação académica personalizada sobre os programas de pós-graduação e MBA da **ENEB Business School** em Angola.

O sistema opera combinando uma **Base de Conhecimento Estruturada em Markdown** com **Prompts de Comportamento e Direcionamento**, permitindo respostas precisas, contextualizadas e sem alucinações via motores como **Google NotebookLM** ou **Gemini API**.

---

## 📐 Diagrama de Arquitetura Conceitual

```text
  [ Candidato / Aluno em Angola ]
                │
                ▼
  ┌───────────────────────────┐
  │   Canal de Atendimento    │  (WhatsApp / Web Chat / Email)
  └─────────────┬─────────────┘
                │
                ▼
  ┌───────────────────────────┐
  │   Motor de IA / RAG Engine│  (NotebookLM / Gemini API)
  └──────┬─────────────┬──────┘
         │             │
         │ RAG Context │ Diretrizes de Comportamento
         ▼             ▼
  ┌─────────────┐   ┌─────────────┐
  │ Knowledge   │   │ Prompts &   │
  │ Base (.md)  │   │ Rules (.md) │
  └─────────────┘   └─────────────┘
         │             │
         └──────┬──────┘
                │
                ▼
  ┌───────────────────────────┐
  │   Resposta Estruturada    │  (Informação + Triagem + Lead)
  └─────────────┬─────────────┘
                │
                ▼
  [ Encaminhamento para a Embaixadoria / Human-in-the-Loop ]
```

---

## 🧩 Componentes Principais

### 1. Camada de Dados (Knowledge Base - `/knowledge_base`)
Contém a informação institucional, factual e regulatória da ENEB. Funciona como a fonte primária de verdade (*Grounding*) para o modelo de linguagem:

- `ENEB_Sobre_Instituicao.md`: História, credenciamento europeu, Universidad Isabel I e acreditação no RUCT.
- `Cursos_ENEB.md`: Catálogo completo de MBAs, Mestrados Especializados, Dupla Titulação e planos de estudo.
- `Processo_Admissao.md`: Requisitos de acesso, documentação necessária e passo a passo de inscrição.
- `Pagamentos.md`: Tabela de propinas, bolsas de estudo de até 80% e métodos de pagamento aceites em Angola.
- `Perguntas_Frequentes.md`: Esclarecimento de dúvidas sobre INAARES, metodologia 100% online e apostilamento de Haia.

### 2. Camada de Orquestração e Comportamento (`/prompts`)
Define a personalidade, as restrições de segurança, os fluxos de diálogo e as regras de negócio do assistente:

- `System_Prompt_Assistant.md`: Prompt mestre com regras de conduta, tom institucional e restrições antialucinação.
- `Atendimento_Candidato.md`: Diretrizes para acolhimento, triagem e captação de dados de contacto (*lead generation*).
- `Orientacao_Academica.md`: Matriz de diagnóstico para recomendação personalizada de cursos com base no perfil do candidato.
- `FAQ_Prompt.md`: Estrutura padronizada de respostas objetivas para dúvidas frequentes.

### 3. Camada de Processamento de IA (RAG Engine)
- **Mecanismo de Busca e Recuperação:** Pesquisa semântica na base de conhecimento para extrair apenas os trechos relevantes para a dúvida do utilizador.
- **Sintetização Contextual:** Utilização do LLM (Gemini / NotebookLM) para gerar respostas fluidas em português europeu/angolano, respeitando estritamente os dados recuperados.

---

## 🔄 Fluxo de Processamento de Mensagens

1. **Entrada do Utilizador:** O candidato envia uma dúvida sobre cursos, reconhecimento ou bolsas.
2. **Contextualização (RAG):** O motor recupera as secções relevantes dos ficheiros da `knowledge_base/`.
3. **Injeção de Instruções:** As diretrizes do `prompts/` aplicam as regras de formato, cordialidade e limites de atuação.
4. **Geração de Resposta:** O modelo formula a resposta, inserindo chamadas para ação (*call to action*) quando apropriado.
5. **Transição / Handoff:** Se o candidato demonstrar interesse de matrícula ou apresentar um caso complexo, o assistente recolhe o Nome, WhatsApp e E-mail para encaminhamento à Embaixadoria em Angola.

---

## 🛡️ Diretrizes de Segurança e Confiabilidade

- **Zero Alucinação:** Se a informação não constar da `knowledge_base/`, o assistente declara explicitamente que irá consultar a Embaixadoria.
- **Conformidade Institucional:** Transparência total sobre a natureza dos títulos (títulos próprios emitidos pela Universidad Isabel I) e o procedimento individual de homologação junto ao INAARES.
- **Proteção de Dados:** Coleta mínima e voluntária de dados de contacto apenas para fins de acompanhamento do processo de admissão.
