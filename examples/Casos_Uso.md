# 🎯 Casos de Uso do Sistema - ENEB Angola AI Assistant

## 🎯 Visão Geral
Este documento descreve os principais **Casos de Uso (Use Cases)** do **ENEB Angola AI Assistant**. Ele define as interações entre os utilizadores (atores) e o sistema de IA, detalhando os cenários funcionais de triagem, consultoria académica, esclarecimento institucional e captação de candidaturas.

---

## 👥 Atores do Sistema

* **Candidato:** Profissional ou estudante em Angola interessado em ingressar num MBA ou Mestrado na ENEB.
* **Aluno Matriculado:** Estudante com matrícula ativa a necessitar de direcionamento sobre o Campus Virtual ou suporte.
* **Assistente Virtual (IA):** O agente inteligente baseado em RAG que processa as dúvidas e orienta a jornada.
* **Embaixadoria ENEB em Angola:** Equipa humana responsável pela validação final da candidatura, emissão da Carta de Admissão e acompanhamento direto.

---

## 📋 Detalhamento dos Casos de Uso

### 🔹 UC01: Triagem e Acolhimento Inicial
* **Ator Principal:** Candidato ou Aluno Matriculado.
* **Objetivo:** Identificar o perfil do interlocutor e saudar com cordialidade institucional.
* **Pré-condições:** O utilizador envia a primeira mensagem em qualquer canal de atendimento.
* **Fluxo Principal:**
  1. O utilizador inicia a conversa.
  2. O assistente saúda e pergunta se o contacto é para obter informações sobre cursos (candidato) ou apoio ao estudo (aluno ativo).
  3. O utilizador indica o seu objetivo.
  4. O assistente direciona o fluxo para orientação académica (UC02) ou suporte pedagógico (UC06).

---

### 🔹 UC02: Consultoria de Orientação Académica e Diagnóstico
* **Ator Principal:** Candidato.
* **Objetivo:** Ajudar o candidato indeciso a escolher a melhor formação (MBA, Mestrado Especializado ou Dupla Titulação).
* **Pré-condições:** O candidato solicita ajuda para selecionar um curso adequado à sua carreira.
* **Fluxo Principal:**
  1. O assistente recolhe informações sobre a licenciatura de base e experiência profissional.
  2. O assistente avalia as aspirações de carreira do candidato.
  3. O assistente apresenta as opções mais recomendadas com base na Matriz de Diagnóstico.
  4. O candidato seleciona o programa pretendido.

---

### 🔹 UC03: Esclarecimento sobre Acreditação e INAARES
* **Ator Principal:** Candidato.
* **Objetivo:** Fornecer informações transparentes e juridicamente alinhadas sobre a validade do diploma europeu em Angola.
* **Pré-condições:** O candidato questiona sobre a acreditação da Universidad Isabel I ou validação no INAARES.
* **Fluxo Principal:**
  1. O candidato questiona a validade do diploma em Angola.
  2. O assistente esclarece a chancela da Universidad Isabel I no RUCT (Espanha) e o procedimento individual de homologação junto do INAARES.
  3. O assistente detalha a disponibilização de documentos com Apostila de Haia.

---

### 🔹 UC04: Consulta de Bolsas de Estudo e Pagamentos
* **Ator Principal:** Candidato.
* **Objetivo:** Informar sobre o Programa de Bolsas de Estudo para Angola (até 80%) e formas de pagamento.
* **Pré-condições:** O candidato pergunta sobre custos, propinas ou modalidades de liquidação.
* **Fluxo Principal:**
  1. O assistente explica as condições da Bolsa de Excelência para Angola.
  2. O assistente enumera os métodos de pagamento aceites (Cartão Internacional, SWIFT, PayPal) e opções de fracionamento.
  3. O assistente convida o candidato a iniciar o processo de admissão para garantir a bolsa (UC05).

---

### 🔹 UC05: Captura e Qualificação de Leads (Handoff)
* **Ator Principal:** Candidato / Embaixadoria ENEB Angola.
* **Objetivo:** Recolher os dados do candidato interessado e transferir para acompanhamento humano.
* **Pré-condições:** O candidato confirma o interesse em formalizar a candidatura ou obter a Carta de Admissão.
* **Fluxo Principal:**
  1. O assistente solicita Nome Completo, E-mail, WhatsApp e Curso pretendido.
  2. O candidato fornece os dados solicitados.
  3. O assistente valida os dados e confirma que a equipa da Embaixadoria entrará em contacto.
  4. Os dados são encaminhados para a equipa humana de admissão em Angola.

---

### 🔹 UC06: Redirecionamento de Suporte a Alunos Ativos
* **Ator Principal:** Aluno Matriculado.
* **Objetivo:** Encaminhar alunos com dúvidas técnicas ou pedagógicas para os canais corretos do Campus Virtual.
* **Pré-condições:** O utilizador identifica-se como aluno já matriculado.
* **Fluxo Principal:**
  1. O assistente identifica que a dúvida se refere ao acesso a matérias, prazos de entrega ou tutoria.
  2. O assistente fornece os canais oficiais de suporte técnico e secretaria académica (`secretaria@eneb.es`).
  3. O assistente oferece apoio local da Embaixadoria em Angola se necessário.

---

## 🔗 Matriz de Mapeamento de Ficheiros por Caso de Uso

| Caso de Uso | Ficheiros de Conhecimento Requeridos | Prompts Utilizados |
|---|---|---|
| **UC01: Triagem Inicial** | `ENEB_Sobre_Instituicao.md` | `System_Prompt_Assistant.md` |
| **UC02: Orientação Académica** | `Cursos_ENEB.md` | `Orientacao_Academica.md` |
| **UC03: Validação & INAARES** | `ENEB_Sobre_Instituicao.md`, `Perguntas_Frequentes.md` | `FAQ_Prompt.md` |
| **UC04: Bolsas & Pagamentos** | `Pagamentos.md`, `Perguntas_Frequentes.md` | `FAQ_Prompt.md` |
| **UC05: Captura de Leads** | `Processo_Admissao.md` | `Atendimento_Candidato.md` |
| **UC06: Suporte a Alunos** | `Perguntas_Frequentes.md` | `System_Prompt_Assistant.md` |
