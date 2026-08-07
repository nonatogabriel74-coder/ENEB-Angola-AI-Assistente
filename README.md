# ENEB-Angola-AI-Assistente
Assistente Inteligente de Informações Acadêmicas baseado em IA Generativa

🤖 Assistente inteligente baseado em IA Generativa e Google NotebookLM para fornecer informações acadêmicas confiáveis ​​​​sobre a ENEB Business School, apoiando candidatos angolanos no processo de inscrição e decisão acadêmica.

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
