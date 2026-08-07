# 🎓 ENEB Angola AI Assistant

> **Assistente Virtual Inteligente de Informações Académicas baseado em IA Generativa e RAG para a ENEB Business School em Angola.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Platform: Google NotebookLM](https://img.shields.io/badge/Platform-Google%20NotebookLM-4285F4?logo=google&logoColor=white)](https://notebooklm.google.com)
[![Language: Markdown](https://img.shields.io/badge/Language-Markdown-000000?logo=markdown&logoColor=white)](#)
[![Scope: ENEB Angola](https://img.shields.io/badge/Scope-ENEB%20Angola-red)](#)

---

## 📌 Visão Geral do Projeto

O **ENEB Angola AI Assistant** é um assistente virtual concebido para revolucionar o atendimento e a orientação académica de candidatos e estudantes angolanos interessados nos programas de MBA, Mestrado e Pós-Graduação da **ENEB Business School**.

Combinando **IA Generativa** e a arquitetura **RAG (Retrieval-Augmented Generation)** através do **Google NotebookLM**, o assistente disponibiliza respostas precisas, contextualizadas e sem alucinações de dados, ancorando-se exclusivamente numa base de conhecimento oficial e curada.

 O projeto alinha-se diretamente com a atuação de **Embaixadoria da ENEB em Angola**, combinando *Gestão do Conhecimento*, *Atendimento ao Cliente*, *Tecnologia Educacional* e *Inteligência Artificial*.

---

## 💡 Problema Identificado vs. Solução Desenvolvida

### ❌ O Problema
Potenciais estudantes e candidatos angolanos enfrentam frequentemente barreiras de informação ao ponderar o ingresso numa instituição europeia online:
- Informações sobre programas, custos e validação dispersas por múltiplos canais.
- Dúvidas recorrentes sobre o funcionamento dos estudos 100% online a partir de Angola.
- Demora nas respostas a questões simples de pré-admissão via e-mail ou formulários.

### ✅ A Solução
Um assistente inteligente que funciona como um **ponto único de verdade ("Tudo sobre a ENEB num único lugar")**:
- **Zero Alucinações:** Responde estritamente com base nos regulamentos e guias oficiais.
- **Linguagem Adequada:** Comunicação adaptada ao contexto do público angolano.
- **Atendimento 24/7:** Orientação imediata sobre requisitos, matrículas, custos e certificação.

---

## 📐 Arquitetura do Sistema

```text
 ┌─────────────────────────────────────────────────────────────────────────────┐
 │                            FONTES OFICIAIS ENEB                             │
 │       (Regulamentos, PDFs de Cursos, Guias Académicos, Preçários)          │
 └──────────────────────────────────────┬──────────────────────────────────────┘
                                        │
                                        ▼
 ┌─────────────────────────────────────────────────────────────────────────────┐
 │                          KNOWLEDGE BASE (Markdown)                          │
 │   knowledge_base/                                                           │
 │     ├── ENEB_Sobre_Instituicao.md     ├── Processo_Admissao.md              │
 │     ├── Cursos_ENEB.md                ├── Pagamentos.md                     │
 │     ├── Documentacao_Necessaria.md    ├── Metodologia_Estudo.md             │
 │     └── Perguntas_Frequentes.md                                             │
 └──────────────────────────────────────┬──────────────────────────────────────┘
                                        │  (Upload de Fontes)
                                        ▼
 ┌─────────────────────────────────────────────────────────────────────────────┐
 │                            GOOGLE NOTEBOOKLM                                │
 │   - Motor de IA Generativa RAG (Retrieval-Augmented Generation)             │
 │   - Ancoragem estrita nas fontes carregadas                                 │
 │   - Aplicação dos Prompts de Instrução do Sistema                           │
 └──────────────────────────────────────┬──────────────────────────────────────┘
                                        │
                                        ▼
 ┌─────────────────────────────────────────────────────────────────────────────┐
 │                        ENEB ANGOLA AI ASSISTANT                             │
 │   - Respostas Contextualizadas e Isentas de Erro                            │
 │   - Suporte ao Candidato via Web / WhatsApp / Canal do Embaixador           │
 └─────────────────────────────────────────────────────────────────────────────┘
```

---

## 📂 Estrutura do Repositório

```text
ENEB-Angola-AI-Assistant/
│
├── README.md                          # Documentação principal do repositório
├── LICENSE                            # Licença de utilização (MIT)
│
├── knowledge_base/                    # Base de conhecimento curada em Markdown
│   ├── ENEB_Sobre_Instituicao.md      # História, acreditação, tripla titulação e modelo
│   ├── Cursos_ENEB.md                 # Catálogo de MBAs, Mestrados e Pós-Graduações
│   ├── Processo_Admissao.md           # Etapas passo a passo da candidatura
│   ├── Documentacao_Necessaria.md     # Requisitos documental para candidatos
│   ├── Pagamentos.md                  # Propinas, bolsas e métodos de pagamento
│   ├── Metodologia_Estudo.md          # Funcionamento do Campus e avaliações
│   └── Perguntas_Frequentes.md        # FAQ oficial cobrindo equivalências e prazos
│
├── prompts/                           # Ficheiros de Engenharia de Prompts
│   ├── System_Prompt_Assistant.md     # Instruções do sistema e regras anti-alucinação
│   ├── Atendimento_Candidato.md       # Fluxo de triagem e captação de candidatos
│   ├── Orientacao_Academica.md        # Diagnóstico para escolha do curso ideal
│   └── FAQ_Prompt.md                  # Estruturação de respostas rápidas
│
├── docs/                              # Documentação técnica do projeto
│   ├── Arquitetura.md                 # Detalhe do fluxo RAG e NotebookLM
│   ├── Metodologia.md                 # Processo de curadoria e auditoria dos dados
│   └── Fluxo_Atendimento.md           # Jornada do candidato do primeiro contacto à matrícula
│
├── examples/                          # Exemplos de testes e validação
│   ├── Conversas_Exemplo.md           # Diálogos reais de simulação
│   └── Casos_Uso.md                   # Matriz de valor e casos de aplicação
│
└── images/                            # Diagramas e recursos visuais
    └── architecture.png               # Diagrama da arquitetura em imagem
```

---

## 🚀 Como Replicar e Executar este Projeto

### 1️⃣ Clonar o Repositório
```bash
git clone https://github.com/SEU_USUARIO/ENEB-Angola-AI-Assistant.git
cd ENEB-Angola-AI-Assistant
```

### 2️⃣ Configurar o Google NotebookLM
1. Aceda ao [Google NotebookLM](https://notebooklm.google.com) e crie um **Novo Bloco de Notas**.
2. Nomeie o bloco como `ENEB Angola AI Assistant`.
3. Faça o upload de todos os ficheiros da pasta `knowledge_base/` como **Fontes**.

### 3️⃣ Aplicar a Engenharia de Prompts
1. Abra o painel de instruções / personalização do chat no NotebookLM.
2. Copie e cole o conteúdo do ficheiro [`prompts/System_Prompt_Assistant.md`](prompts/System_Prompt_Assistant.md).
3. Teste o assistente submetendo perguntas de validação (consulte [`examples/Conversas_Exemplo.md`](examples/Conversas_Exemplo.md)).

---

## 🎯 Casos de Uso Principais

| # | Caso de Uso | Descrição | Impacto |
|---|---|---|---|
| 1 | **Atendimento Inicial (WhatsApp/Web)** | Atendimento automático às dúvidas mais frequentes enviadas à embaixadoria | Redução de até **80%** no tempo gasto com respostas repetitivas |
| 2 | **Apoio à Decisão Académica** | Orientação personalizada sobre se o candidato deve escolher MBA ou Mestrado | Aumento da taxa de conversão e adesão dos candidatos |
| 3 | **Onboarding do Aluno Admitido** | Explicação prática sobre como aceder ao Campus Virtual e submeter trabalhos | Redução da ansiedade inicial e melhoria na retenção de alunos |
| 4 | **Inovação no Recrutamento** | Demonstração de uso de IA aplicada ao setor da educação online em Angola | Fortalecimento do posicionamento institucional da marca ENEB |

---

## 🛠️ Tecnologias Utilizadas

- **[Google NotebookLM](https://notebooklm.google.com):** Ambiente RAG baseado nos modelos Gemini para consulta ancorada.
- **Inteligência Artificial Generativa:** Processamento de linguagem natural e síntese de informação.
- **Engenharia de Prompts:** Técnicas de ancoragem (*grounding*), *system prompts* delimitados e prevenção de alucinações.
- **Gestão do Conhecimento:** Curadoria, estruturação e padronização de fontes institucionais em Markdown.
- **Git & GitHub:** Controlo de versão e documentação do projeto.

---

## 👨‍💻 Autor & Responsável

**Nonato Matondo Gabriel**
* *Embaixador ENEB Angola*
* *Founder & Developer do ENEB Angola AI Assistant*
* *Especialista em Gestão de Projetos, Big Data e IA Generativa*

---

## 📜 Licença

Este projeto é disponibilizado sob a licença [MIT](LICENSE) - sinta-se à vontade para utilizar, adaptar e contribuir.


