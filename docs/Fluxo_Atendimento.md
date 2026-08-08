# 🔄 Fluxo de Atendimento e Jornada do Candidato - ENEB Angola AI Assistant

## 🎯 Visão Geral
Este documento especifica o fluxo operacional e relacional de atendimento ao cliente/candidato aplicado pelo **ENEB Angola AI Assistant**. O objetivo principal é estruturar a jornada desde o primeiro contacto do interessado até ao encaminhamento qualificado (*lead handoff*) para a equipa da Embaixadoria ENEB em Angola.

---

## 🗺️ Mapeamento das Etapas do Fluxo

```text
 [ Entrada do Candidato ]
            │
            ▼
 ┌─────────────────────────┐
 │ 1. Boas-Vindas &        │
 │    Triagem Inicial      │
 └──────────┬──────────────┘
            │
            ├───────────────────────────────┐
            ▼                               ▼
 ┌─────────────────────────┐     ┌─────────────────────────┐
 │ 2A. Orientação          │     │ 2B. Esclarecimento      │
 │     Académica & Perfil  │     │     de FAQ / Admissão   │
 └──────────┬──────────────┘     └──────────┬──────────────┘
            │                               │
            └──────────────┬────────────────┘
                           │
                           ▼
 ┌─────────────────────────────────────────┐
 │ 3. Apresentação da Proposta de Valor    │
 │    (Bolsas de Estudo 80% / Flexibilidade) │
 └─────────────────────────┬───────────────┘
                           │
                           ▼
 ┌─────────────────────────────────────────┐
 │ 4. Captura de Dados & Qualificação      │
 │    (Nome, E-mail, WhatsApp, Curso)      │
 └─────────────────────────┬───────────────┘
                           │
                           ▼
 ┌─────────────────────────────────────────┐
 │ 5. Encaminhamento para Embaixadoria     │
 │    (Acompanhamento Humano & Admissão)   │
 └─────────────────────────────────────────┘
```

---

## 📋 Detalhamento das Etapas da Jornada

### Etapa 1: Boas-Vindas e Triagem Inicial
* **Gatilho:** Primeira mensagem recebida do utilizador.
* **Ação da IA:** 
  * Saudar cordialmente o utilizador.
  * Identificar se é um **potencial candidato** (interessado em bolsas/cursos) ou um **aluno matriculado** em busca de suporte no Campus.
* **Exemplo de Intervenção:**
  > *"Olá! Seja muito bem-vindo(a) à ENEB Business School Angola. Sou o assistente virtual oficial da Embaixadoria. Procura informação sobre os nossos cursos de MBA/Mestrado ou já é nosso aluno?"*

---

### Etapa 2A: Orientação Académica e Diagnóstico de Perfil
* **Gatilho:** Candidato indeciso ou à procura do programa mais adequado.
* **Ação da IA:**
  * Aplicar as perguntas de diagnóstico (formação anterior, objetivos profissionais, disponibilidade).
  * Recomendar o programa mais alinhado (MBA, Mestrado Especializado ou Dupla Titulação).
* **Critério de Transição:** Quando o candidato demonstra preferência por um curso específico.

---

### Etapa 2B: Esclarecimento de FAQ, Admissão e Propinas
* **Gatilho:** Perguntas diretas sobre reconhecimento INAARES, metodologia 100% online, valores ou pagamentos.
* **Ação da IA:**
  * Responder com objetividade baseando-se na `knowledge_base/`.
  * Destacar o respaldo europeu (Universidad Isabel I) e a flexibilidade sem exames presenciais.

---

### Etapa 3: Apresentação da Proposta de Valor
* **Ação da IA:**
  * Apresentar o Programa de Bolsas de Estudo de Excelência para Angola (até 80% de desconto).
  * Explicar as condições facilitadas de pagamento e o apoio personalizado da Embaixadoria local.

---

### Etapa 4: Captura de Dados do Candidato (Lead Generation)
* **Gatilho:** O candidato expressa interesse em candidatar-se, obter bolsa ou receber a carta de admissão.
* **Ação da IA:**
  * Solicitar de forma profissional os dados mínimos para registo e contacto:
    1. **Nome Completo**
    2. **Endereço de E-mail**
    3. **Contacto Telefónico / WhatsApp**
    4. **Curso pretendido**

---

### Etapa 5: Encaminhamento para a Embaixadoria (Handoff)
* **Ação da IA:**
  * Confirmar a receção dos dados.
  * Explicar que a equipa do Embaixador ENEB em Angola entrará em contacto direto via WhatsApp/E-mail para formalizar a candidatura, emitir a Carta de Admissão e guiar no processo de bolsa.

---

## 🛑 Tratamento de Casos Especiais e Exceções

| Cenário de Exceção | Comportamento Requerido da IA |
|---|---|
| **Dúvida não constante da Base de Conhecimento** | Declarar honestamente a falta da informação específica e agendar o contacto da Embaixadoria para esclarecimento. |
| **Aluno com problema técnico no Campus Virtual** | Orientar o envio de e-mail para o suporte académico (`secretaria@eneb.es` ou canal interno do aluno) e notificar a equipa local. |
| **Dúvidas sobre vistos / deslocação para Espanha** | Relembrar que a metodologia é **100% online**, dispensando viagem a Espanha ou visto de estudante. |
