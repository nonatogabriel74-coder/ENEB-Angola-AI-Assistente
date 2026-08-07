# ENEB-Angola-AI-Assistente
Assistente Inteligente de Informações Acadêmicas baseado em IA Generativa

📌 Visão Geral

O ENEB Angola AI Assistant é um projeto de Inteligência Artificial Generativa desenvolvido para criar um assistente inteligente capaz de fornecer informações organizadas, confiáveis e contextualizadas sobre a ENEB Business School.

A solução usa o Google NotebookLM como base de conhecimento, permitindo a criação de um ambiente de consulta inteligente baseado em documentos previamente selecionados.

O objetivo principal é facilitar o acesso à informação acadêmica para candidatos angolanos, oferecendo respostas rápidas sobre processos de candidatura, programas acadêmicos, metodologia de estudo e outros temas relacionados à jornada do estudante.

🎯 Objetivos do Projeto

Objetivo Geral

Desenvolver um assistente virtual baseado em IA Generativa para apoiar candidatos interessados nos programas académicos da ENEB.

Objetivos Específicos

Centralizar informações acadêmicas em uma única base de conhecimento.
Aplicar técnicas de Engenharia de Prompts.
Melhorar a experiência de pesquisa dos candidatos.
Reduzir dúvidas repetitivas no processo de atendimento.
Demonstrar aplicação prática de IA Generativa na educação.
Crie uma solução escalável para suporte acadêmico.

🧩 Problema identificado

Durante o processo de decisão académica, muitos candidatos enfrentam dificuldades para encontrar informações claras sobre:

Processo de candidatura;
Requisitos de ingresso;
Programas disponíveis;
Funcionamento da modalidade online;
Métodos de pagamento;
Processo acadêmico;
Certificação.

As informações podem estar distribuídas por diferentes canais, tornando o processo mais demorado.

💡 Solução Desenvolvida

O projeto propõe um assistente inteligente que utiliza uma base documental organizada para responder perguntas dos utilizadores.

O funcionamento baseia-se em:
Recolha de informação;
Organização documental;
Criação da base de conhecimento;
Configuração do NotebookLM;
Aplicação de prompts especializados;
Geração de respostas contextualizadas.

🏗️ Arquitetura da Solução

Fluxo do sistema:

Documentos Institucionais
          ↓
Base de Conhecimento
          ↓
Google NotebookLM
          ↓
Prompt Engineering
          ↓
ENEB Angola AI Assistant
          ↓
      Utilizador

📚 Base de Conhecimento

A informação do assistente é organizada nos seguintes módulos:

knowledge_base/

├── Sobre_ENEB.md

├── Programas_Academicos.md

├── Processo_Admissao.md

├── Processo_Inscricao.md

├── Documentacao_Necessaria.md

├── Pagamentos.md

├── Metodologia_Estudo.md

├── Certificacao.md

└── FAQ.md

🚀 Funcionalidades

Informação Institucional

Permite consultar informações gerais sobre a ENEB:
História;
Modelo educativo;
Formação online;
Público-alvo.

Programas Acadêmicos
Consulta informações relacionadas com:
MBA;
Mestrados;
Pós-graduações;
Especializações.

Orientação ao Candidato

O assistente ajuda com perguntas como:
Como iniciar a candidatura?
Que documentos são necessários?
Como funciona o estudo online?
Qual programa escolher?

Perguntas Frequentes (FAQ)
Responde dúvidas comuns usando a base documental disponível.

🛠️ Tecnologias Utilizadas

Tecnologia	Aplicação

Google NotebookLM	Base de conhecimento e consulta inteligente
Inteligência Artificial Generativa	Processamento e geração de respostas
Engenharia de Prompts	Configuração do comportamento do assistente
Espaço de trabalho do Google	Organização documental
GitHub	Gestão e documentação do projeto

📂 Estrutura do Repositório

ENEB-Angola-AI-Assistant/

│
├── README.md

├── assets/

│   └── banner.png


├── images/

│   └── architecture.png


├── knowledge_base/

│   ├── Sobre_ENEB.md

│   ├── Programas_Academicos.md

│   ├── Processo_Admissao.md

│   ├── Processo_Inscricao.md

│   ├── Documentacao.md

│   ├── Pagamentos.md

│   ├── Metodologia_Estudo.md

│   ├── Certificacao.md

│   └── FAQ.md


├── prompts/

│   ├── System_Prompt.md

│   ├── Atendimento_Candidato.md

│   └── Regras_Assistente.md


├── docs/

│   ├── Arquitetura.md

│   ├── Metodologia.md

│   └── Fluxo_Processo.md


└── casos_uso/

    ├── Novo_Candidato.md

    ├── Escolha_Programa.md

    └── Suporte_Academico.md
    
⚙️ Configuração do Projeto

Pré-requisitos
Conta Google;
Acesso ao Google NotebookLM;
Documentação institucional organizada.
Processo de Implementação

1. Preparação dos documentos
Organizar todos os conteúdos na pasta:
knowledge_base/

2. Criar Notebook no Google NotebookLM
Adicionar os documentos como fontes de conhecimento.

3. Configurar o Prompt do Assistente

Exemplo:

Você é o ENEB Angola AI Assistant.
Responda exclusivamente com base nas fontes disponíveis.
Não invente informações.
Quando não encontrar uma resposta,
indique que a informação deve ser confirmada oficialmente.

💬 Exemplos de Utilização

Pergunta

Como faço para ingressar na ENEB?

Resposta esperada
O candidato deve selecionar o programa pretendido,
verificar os requisitos disponíveis e seguir
o processo oficial de candidatura.

📌 Casos de uso

Caso 1 — Novo candidato
Mirar:
Orientar pessoas interessadas em iniciar uma formação.

Caso 2 — Escolha acadêmica
Mirar:
Ajudar candidatos a compreenderem os programas disponíveis.

Caso 3 — Atendimento acadêmico
Mirar:
Reduzir perguntas repetitivas e melhorar a experiência do usuário.

🔐 Princípios do Assistente

O projeto segue boas práticas:
Respostas baseadas em fontes;
Transparência da informação;
Redução de alucinações da IA;
Organização do conhecimento;
Uso responsável da Inteligência Artificial.

🗺️ Roteiro

Versão 1.0
 Estrutura do projeto
 Base de conhecimento
 Pergunta inicial
 Documentação técnica
 
Versão 2.0
 Interface Web
 chatbot integrado
 WhatsApp Business
 Dashboard de interações
 
Versão 3.0
 Analytics de candidatos
 Automação comercial
 Integração CRM

 
👨‍💻 Autor
Obrigado Gabriel
Projeto Independente — 2026

Áreas:
Inteligência Artificial Generativa
Engenharia de Prompts
Inteligência de Negócios
Gestão do Conhecimento
Transformação Digital

📄 Licença
Este projeto está disponível sob licença MIT.
