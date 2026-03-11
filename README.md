# 🎯 Desafio Técnico QA - Beedoo (2026)

## 📌 Objetivo da Aplicação
A aplicação em teste consiste em um módulo web para **Cadastro e Listagem de Cursos**. O sistema possui campos de texto, numéricos, datas (com calendário), URLs de imagens e renderização condicional (modalidade Presencial vs Online). O objetivo deste projeto foi mapear cenários de testes, executar validações de Front-end/Back-end e reportar os defeitos encontrados, visando garantir a qualidade e resiliência do software.

## 🔄 Principais Fluxos e Regras Mapeadas
1. **Fluxo de Cadastro (Caminho Feliz):** Preenchimento de todos os dados (Título, Descrição, Instrutor, Datas, Imagem, Vagas e Modalidade) e submissão com sucesso.
2. **Renderização Condicional:** Comportamento da interface ao alternar entre curso "Online" (exigindo Link) e "Presencial" (exigindo Endereço).
3. **Validação de Exceções e Limites (Boundary):** Comportamento do sistema ao receber dados em branco, textos que excedem limites, números irreais de vagas e datas retroativas/inconsistentes.
4. **Segurança (Sanitização):** Testes de injeção de scripts (XSS) nos campos de texto.

## ⚠️ Pontos Críticos Identificados (Resumo)
Durante a execução, foram encontrados **9 bugs**, sendo os mais críticos:
* **Falso Positivo na Exclusão:** O sistema informa que o curso foi deletado, mas não efetiva a ação.
* **Quebra de Layout (UI/UX):** A tela de listagem não organiza os cards corretamente, gerando sobreposição e inviabilizando o uso.
* **Falta de Validação de Dados:** O sistema aceita formulários 100% em branco, datas de término anteriores ao início, e não possui limite máximo para o campo numérico de vagas.

## 🔗 Entregáveis
* 📊 **[Planilha de Casos de Teste e Bugs]** -> `(https://docs.google.com/spreadsheets/d/1FhkTd9XmNUY3J9G8EhsqHXDsUy3OJZtapr-xN-_vIBA/edit?usp=sharing)`
* 📁 **[Evidências (Prints dos Bugs)]** -> `(https://drive.google.com/drive/folders/1LXpOLBo1ib9FLfG2prfVmIvotFJq7jog?usp=sharing)`
