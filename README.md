# 🛡️ Miniguia de Estudos - OWASP Top 10 com NotebookLM

## 📌 Contexto e Objetivos

Este repositório documenta a criação de um **Caderno Temático (NotebookLM)** focado no estudo da **OWASP Top 10**, a principal referência mundial para identificação dos riscos mais críticos em segurança de aplicações web.

**Objetivos de estudo:**

- Compreender em profundidade as 10 categorias de risco da OWASP Top 10 (versões 2021 e 2025).
- Dominar técnicas de **descoberta** (como identificar a falha) e **prova de conceito** (como reproduzi-la em ambiente controlado).
- Aprender a **mitigar** e **corrigir** cada vulnerabilidade com boas práticas de código, configuração e ferramentas de segurança.
- Consolidar o conhecimento através de exemplos práticos e fictícios.
- Internalizar a **postura ética** necessária para aplicar esse conhecimento exclusivamente em segurança ofensiva autorizada e aprendizagem.

---

## 📚 Curadoria de Fontes

Para alimentar o NotebookLM, foram utilizadas as seguintes fontes oficiais e complementares:

### Fontes Oficiais OWASP

| Fonte | Descrição |
|-------|-----------|
| [OWASP Top 10:2025](https://owasp.org/Top10/2025/) | Versão mais recente do documento oficial, com a lista atualizada dos riscos mais críticos. |
| [OWASP Top 10:2021](https://owasp.org/Top10/2021/) | Versão anterior, mantida para fins de comparação e estudo histórico. |
| [Repositório Oficial OWASP/Top10](https://github.com/OWASP/Top10) | Repositório oficial com todas as versões do documento, incluindo apresentações e PDFs. |
| [OWASP Top 10:2021 - A04 Insecure Design](https://owasp.org/Top10/2021/A04_2021-Insecure_Design/) | Página detalhada sobre a categoria "Insecure Design", com exemplos e mitigação. |
| [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/) | Projeto complementar focado em vulnerabilidades específicas de aplicações móveis. |

### Ferramentas e Guias Práticos

| Fonte | Descrição |
|-------|-----------|
| [Free for Open Source Application Security Tools](https://owasp.org/www-community/Free_for_Open_Source_Application_Security_Tools) | Lista de ferramentas SAST, DAST e IAST gratuitas para projetos open source. |
| [OWASP SCP Quick Reference Guide v2](https://iotsecuritymapping.com/wp-content/uploads/2022/05/OWASP_SCP_Quick_Reference_Guide_v2.pdf) | Guia rápido de referência sobre Secure Coding Practices. |
| [Broken Access Control Prevention Guide](https://info.veracode.com/rs/790-ZKW-291/images/broken-access-control-prevention-guide-en.pdf) | Guia prático da Veracode sobre prevenção de quebras de controle de acesso. |

### Artigos e Conteúdo Complementar

| Fonte | Descrição |
|-------|-----------|
| [Integrate OWASP Top 10 in Your Development Workflow](https://cyber-security-in-plain-english.com/post/developers/organization/integrate-owasp-10-in-to-your-development-workflow/) | Artigo sobre como integrar a OWASP Top 10 no ciclo de desenvolvimento. |
| [OWASP Overview](https://rafter.so/blog/owasp-overview) | Visão geral da OWASP e sua importância para a segurança de aplicações. |
| [OWASP Top 10 Hands-On Labs](https://learn.secbyte.org/blog/owasp-top-10-hands-on-labs) | Laboratórios práticos para aprender as vulnerabilidades na prática. |

### Fontes em Vídeo

| Fonte | Descrição |
|-------|-----------|
| [Vídeo 1](https://www.youtube.com/watch?v=k9o7AbjLDTs) | Introdução à OWASP Top 10 e principais conceitos. |
| [Vídeo 2](https://www.youtube.com/watch?v=v9M1hFf4xyo) | Aprofundamento em vulnerabilidades específicas. |

### Acesso ao NotebookLM

O caderno temático pode ser acessado através do link:
🔗 [NotebookLM - OWASP Top 10 Study](https://notebook.google.com/notebook/5157ede4-f2e9-487f-8b47-3378c9c602f1)

---

## 🧠 Engenharia de Prompts e "Cicatrizes"

Esta seção documenta os prompts estratégicos utilizados no NotebookLM, as respostas obtidas e as dificuldades encontradas durante o processo de extração de conhecimento.

### Prompt 1 - Visão Geral Comparativa

**Prompt:**
> "Com base nas fontes carregadas, crie uma tabela comparativa entre a OWASP Top 10:2021 e a OWASP Top 10:2025. Para cada categoria, destaque as principais mudanças, novas inclusões e categorias removidas. Inclua uma breve descrição de cada risco."

**Resposta esperada:** Tabela com as 10 categorias de cada versão, indicando quais foram mantidas, renomeadas, removidas ou adicionadas.

**Cicatriz (dificuldade):** O NotebookLM inicialmente trouxe apenas a lista de 2025. Foi necessário refinar o prompt para incluir a comparação explícita com a versão 2021.

---

### Prompt 2 - Foco em Descoberta e Prova de Conceito

**Prompt:**
> "Para a categoria 'Broken Access Control' (A01:2025), detalhe como um pentester pode descobrir essa falha em uma aplicação web. Descreva passo a passo uma prova de conceito (PoC) em um ambiente de teste fictício. Inclua exemplos de requisições HTTP e como o atacante pode explorar a falha."

**Resposta esperada:** Guia passo a passo com exemplos de requisições, ferramentas sugeridas (como Burp Suite) e cenários de exploração.

**Cicatriz (dificuldade):** O NotebookLM foi muito genérico na primeira tentativa. **Solução:** Especificar um cenário concreto: "Use o exemplo de um e-commerce fictício onde o usuário pode acessar o pedido de outro cliente alterando o ID na URL."

---

### Prompt 3 - Mitigação com Código

**Prompt:**
> "Para cada uma das 10 vulnerabilidades da OWASP Top 10:2025, apresente um código de exemplo (em Python com Flask) que contenha a falha e, em seguida, o mesmo código corrigido com a mitigação adequada. Explique por que a correção resolve o problema."

**Resposta esperada:** Pares de código (vulnerável vs. corrigido) com explicações técnicas.

**Cicatriz (dificuldade):** O NotebookLM gerou exemplos em linguagens variadas. **Solução:** Especificar a linguagem desejada no prompt.

---

### Prompt 4 - Ferramentas de Segurança

**Prompt:**
> "Liste as principais ferramentas SAST, DAST e IAST gratuitas para projetos open source, conforme mencionado nas fontes. Para cada ferramenta, indique sua finalidade, linguagens suportadas e como integrá-la em um pipeline de CI/CD."

**Resposta esperada:** Lista detalhada de ferramentas com especificações técnicas.

**Cicatriz (dificuldade):** O NotebookLM confundiu ferramentas pagas com gratuitas. **Solução:** Refinar com "apenas ferramentas que são totalmente gratuitas para projetos open source".

---

### Prompt 5 - Glossário

**Prompt:**
> "Crie um glossário com os principais termos técnicos utilizados nas fontes sobre OWASP Top 10. Para cada termo, forneça uma definição clara e um exemplo de uso no contexto de segurança de aplicações."

**Resposta esperada:** Lista de termos como *Broken Access Control*, *Security Misconfiguration*, *SSRF*, *CWE*, *Salting*, *SAST*, *DAST*, etc.

---

### Prompt 6 - Guia de Estudo para Revisão

**Prompt:**
> "Com base em todas as fontes, crie um guia de estudo para revisão da OWASP Top 10:2025. O guia deve conter: (1) um resumo de uma página por categoria, (2) 3 perguntas de fixação por categoria com respostas, (3) um mapa mental dos principais conceitos."

**Resposta esperada:** Documento estruturado para revisão rápida.

---

## 📖 Miniguia de Estudo

### Resumo Estruturado da OWASP Top 10:2025

| Posição | Categoria | Descrição Resumida | Exemplo Fictício | Mitigação |
|---------|-----------|-------------------|------------------|-----------|
| **A01** | Broken Access Control | Usuários acessam recursos fora de suas permissões. | Cliente altera ID na URL e vê dados de outro usuário. | Validar acesso no servidor; princípio do menor privilégio. |
| **A02** | Security Misconfiguration | Configurações inseguras em servidores, apps ou containers. | Painel admin exposto na internet sem autenticação. | Automatizar revisões; aplicar hardening. |
| **A03** | Software Supply Chain Failures | Dependências externas comprometidas. | Pacote NPM malicioso rouba dados do usuário. | Validar integridade com hashes; revisar dependências. |
| **A04** | Cryptographic Failures | Uso incorreto ou ausência de criptografia. | Senhas armazenadas com MD5 ou SHA1. | Usar AES, SHA-256, TLS 1.3; gerenciar chaves com HSMs. |
| **A05** | Injection | Inserção de comandos maliciosos em entradas. | SQL Injection em campo de busca. | Usar consultas parametrizadas (prepared statements). |
| **A06** | Insecure Design | Falhas no design da aplicação. | Arquitetura que não prevê separação de privilégios. | Adotar threat modeling desde o design. |
| **A07** | Authentication Failures | Falhas no processo de autenticação. | Senhas fracas ou ausência de MFA. | Implementar MFA; políticas de senha fortes. |
| **A08** | Software and Data Integrity Failures | Falhas na integridade de software e dados. | Atualizações sem verificação de assinatura. | Assinar artefatos; verificar integridade. |
| **A09** | Logging & Alerting Failures | Falhas de log e monitoramento. | Ataque não é detectado por falta de logs. | Implementar logs detalhados e alertas. |
| **A10** | Mishandling of Exceptional Conditions | Tratamento inadequado de exceções. | Erro expõe stack trace com informações sensíveis. | Tratar exceções sem vazar dados internos. |

---

### Glossário dos Principais Conceitos

| Termo | Definição |
|-------|-----------|
| **OWASP** | Open Web Application Security Project - organização sem fins lucrativos focada em segurança de software. |
| **Broken Access Control** | Falha que permite a usuários acessarem recursos ou executarem ações fora de suas permissões. |
| **Security Misconfiguration** | Configuração insegura de servidores, frameworks ou permissões. |
| **Software Supply Chain** | Cadeia de suprimentos de software, incluindo dependências e pipelines de CI/CD. |
| **Cryptographic Failure** | Uso incorreto ou ausente de criptografia para proteger dados sensíveis. |
| **Injection** | Inserção de comandos maliciosos em entradas de sistemas. |
| **Insecure Design** | Vulnerabilidades decorrentes de falhas no design da aplicação, não apenas no código. |
| **SAST** | Static Application Security Testing - análise estática de código fonte para identificar vulnerabilidades.[reference:8] |
| **DAST** | Dynamic Application Security Testing - análise dinâmica de aplicações em execução.[reference:9] |
| **IAST** | Interactive Application Security Testing - combina técnicas SAST e DAST durante a execução.[reference:10] |
| **CWE** | Common Weakness Enumeration - lista padronizada de fraquezas de software. |
| **PoC (Proof of Concept)** | Demonstração prática de como uma vulnerabilidade pode ser explorada. |
| **Mitigação** | Ação ou controle implementado para reduzir o risco de uma vulnerabilidade. |
| **Salting** | Técnica de adicionar um valor aleatório (salt) às senhas antes de aplicar hash. |
| **Threat Modeling** | Processo de identificação e avaliação de ameaças durante a fase de design. |

---

### Conjunto de Prompts Reutilizáveis

```markdown
1. "Resuma a OWASP Top 10:2025 em uma tabela com nome, descrição, exemplo e mitigação."

2. "Compare a OWASP Top 10:2021 com a 2025. Quais foram as principais mudanças?"

3. "Para a categoria [X], detalhe como descobrir a falha e crie uma prova de conceito (PoC)."

4. "Mostre um código vulnerável e o código corrigido para a vulnerabilidade [Y] em Python/Flask."

5. "Liste ferramentas SAST, DAST e IAST gratuitas para projetos open source."

6. "Crie um glossário com os principais termos da OWASP Top 10."

7. "Gere 5 perguntas de múltipla escolha sobre a OWASP Top 10:2025 para eu testar meus conhecimentos."

8. "Explique a diferença entre [Categoria A] e [Categoria B] com exemplos práticos."

9. "Monte um plano de estudos de 7 dias para aprender a OWASP Top 10:2025 do zero."

10. "Para cada vulnerabilidade, indique ferramentas que podem ser usadas para detectá-la."

11. "Crie um mapa mental interligando as 10 categorias da OWASP Top 10:2025."

12. "Como integrar a OWASP Top 10 no pipeline de CI/CD de uma empresa?"
