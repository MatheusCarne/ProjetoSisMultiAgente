# 📄 Relatório de Acompanhamento de Projeto — Sistemas Multiagente

> Preencha com atenção. Este relatório tem o objetivo de **organizar o pensamento, identificar bloqueios e alinhar os próximos passos do seu projeto**.

---

## 🧠 1. Visão Geral do Projeto

- **Título do Projeto**:  
  Detecção e Contagem de Pessoas com Geração Automática de Relatórios usando Arquitetura Multiagente

- **Integrantes da Equipe**:  
  - Matheus Carneiro
  - Lucas Daris

- **Resumo em uma frase**:  
  Sistema baseado em agentes inteligentes para detecção e contagem de pessoas em imagens, com capacidade de gerar relatórios automáticos via LLMs.

---

## ⚙️ 2. Arquitetura Atual

- **Quantos agentes existem no sistema atualmente?**  
  - Agente detector
  - Agente Analista
  - Agente redator

- **Função principal de cada agente:**  
  - Agente de Visão (que usa a ferramenta YOLO)
  - Agente Analista (que poderia processar os dados JSON)
  - Agente de Relatório (que escreve o texto final)

- **Eles interagem entre si? Como?**
 
| Etapa | Agente Responsável   | Input Principal           | Output (Contexto para o Próximo)     |
| :---- | :------------------- | :------------------------ | :----------------------------------- |
| **1** | Agente de Visão      | Caminho da imagem         | Dados brutos (JSON com a contagem)   |
| **2** | Agente Analista      | Dados brutos da Etapa 1   | Dados processados (Sumário em texto) |
| **3** | Agente de Relatório  | Sumário da Etapa 2        | Relatório final em linguagem natural |


- **Já existe algum ambiente de simulação/teste?**  
  A principio o projeto esta sendo feito no Google Colab, porem estou tendo alguns problemas.

---

## ✅ 3. Avanços Concretos

- Integração de Visão Computacional com um Framework de LLM.
- Configuração de um Pipeline Automatizado de Ponta a Ponta.

---

## 🧱 4. Dificuldades Enfrentadas

- Ambiente de Desenvolvimento Instável, varios erros de ImportError, ValidationError, conflitos de versão e ResolutionImpossible.
- Dificuldade para o agente utilizar a ferramenta desenvolvida de detecção.

---

## 🛠️ 5. Estratégias de Superação

- Tentar desenvolver o projeto localmente ao inves do Colab.

---

## 🎯 6. Próximos Passos

- Conseguir fazer o agente detector utilizar corretamente a ferramenta com YOLO.
- Construir o Agente Analista
- O LLM do Agente Analista ser ativado com um prompt que combina sua instrução e o contexto.
- Construir o Agente Redator que gera o texto final do relatório.

---

## 📢 7. Pedido de Ajuda

- A principio a ideia era desevolver um codigo de detecção de pessoas e posteriormente com os resultados isso ser passado para um LLM gerar os relatorios, porem vi que daria para criar um agente que use nosso codigo de detecção como uma ferramenta, se encaixaria melhor na proposta da disciplina, porem estou com alguns problemas para implementar desse novo jeito a parte de ferramenta e a questão é:

✅ Opção 1: Manter o código de detecção como está + usar LLM apenas para relatório
- Estrutura:
- O código do YOLO continua como um script normal (sem agente).
- Após a detecção, os resultados (ex: JSON, CSV, ou texto) são enviados para uma LLM (como o ChatGPT ou Crew AI).
- A LLM gera o relatório de forma autônoma, interpretando os dados.

✅ Vantagens:
- Mais simples e direto.
- Menos trabalho de reestruturação.
- Foco rápido em análise e geração de insights.

❌ Limitações:
- Pouca modularidade.
- Difícil escalar ou adicionar novos comportamentos (ex: rastreamento, decisão, notificações, etc).
- Os agentes não colaboram entre si.

🧠 Opção 2: Transformar o código de detecção em um agente e integrá-lo com o agente de relatório (multiagentes)
- Estrutura:
- Um Agente de Detecção encapsula e executa o YOLO.
- Um Agente de Relatório solicita os dados do agente de detecção e gera um relatório.
- Toda a interação é organizada e autônoma (pode até escalar para incluir rastreamento, alarmes, etc.).

✅ Vantagens:
- Arquitetura modular e expansível.
- Pode usar Crew AI ou frameworks multiagentes como SPADE ou JADE.
- Mais próxima de sistemas reais de IA distribuída.

❌ Limitações:
- Mais complexa de implementar inicialmente.
- Requer reestruturação do código atual.
- Exige mais controle da comunicação entre os agentes.

---
