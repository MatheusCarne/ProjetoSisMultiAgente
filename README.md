# 🧠 Detecção e Contagem de Pessoas com Geração Automática de Relatórios usando Arquitetura Multiagente
## 👨‍🎓 Integrantes

<div style="display: inline_block;" align="center">

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/MatheusCarne" target="_blank">
        <img src="https://avatars.githubusercontent.com/u/88046644?v=4" width="100px;" alt="Avatar Matheus"/><br>
        <sub>
          <b>Matheus Carneiro | 202111250033</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/LucasByteX" target="_blank">
        <img src="https://avatars.githubusercontent.com/u/105729815?v=4" width="100px;" alt="Avatar Lucas"/><br>
        <sub>
          <b>Lucas Daris | 202021250037</b>
        </sub>
      </a>
    </td>
  </tr>
</table>

</div>

## 💡 Ideia Principal
O projeto consiste em um sistema baseado em agentes inteligentes para **detecção e contagem de pessoas** em ambientes públicos, com capacidade de **gerar relatórios automáticos** via modelos de linguagem (LLMs).

https://github.com/user-attachments/assets/650c8eb8-a342-4a15-b14f-f9678c4812f4

## 🎯 Objetivos
- Criar um sistema descentralizado e modular, com agentes inteligentes.
- Detectar, contar e rastrear pessoas com alta precisão.
- Gerar relatórios automáticos por LLM com base nos dados coletados.
- Possibilidade de dashboard em tempo real com alertas de lotação.
- Possibilidade futura de prever padrões de movimentação.

## 👥 Público-Alvo
Empresas e governos que precisam monitorar o fluxo de pessoas em locais públicos para otimizar serviços e segurança.

## 🤖 Arquitetura

- **🧠 Motor de Rastreamento (Tracking Engine)**  
  Utiliza Ultralytics, código especializado que fornece dados ao restante do sistema.

- **📊 Agente de Análise (Analista)**  
  Recebe os dados de rastreamento e os processa para gerar estatísticas.

- **📝 Agente de Relatório (LLM Reporter)**  
  Utiliza um modelo de linguagem (como GPT-4 ou LLaMA) para transformar dados quantitativos em relatórios descritivos.

## 🧱 Tecnologias Pretendidas
- **Linguagem de Programação:** Python  
  > Escolhida por ser amplamente usada em aplicações de visão computacional e possuir grande variedade de bibliotecas especializadas.

- **Bibliotecas e Frameworks:**
  - **Ultralytics TrackZone YOLO11m-pose / OpenCV**: Para detecção de pessoas.  
    > YOLO é rápido e eficiente para detecção em tempo real.
  - **TrackZone**: Para rastreamento de indivíduos.  
    > Permite identificar e seguir pessoas ao longo de múltiplos frames, evitando duplicações.
  - **OpenCV**: Para pré-processamento de imagens e manipulação de vídeo.  
  - **GPT-4 ou LLaMA**: Geração Automática de Relatórios.
    > Um LLM pode analisar os dados de movimentação (fluxo por horário, local, etc.) e gerar relatórios descritivos automaticamente.
      
- **Ferramentas de Visualização:**  
  - Bibliotecas de gráficos (como Plotly ou Matplotlib) para visualização no dashboard.  

## 📦 Entradas e Saídas Esperadas
**Entradas:**
- Vídeos ou imagens de câmeras em tempo real.
- Parâmetros de configuração (como zonas de interesse ou limite de lotação).

**Entradas para os agentes:**
- json com todos os dados de rastreio feito pelo TrackZone.

**Saídas:**
- json com todos os dados de rastreio feito pelo TrackZone.
- Video processado com as pessoas rastreadas conforme configuração.
- Relatórios e gráficos sobre fluxo de pessoas ao longo do rastreio.
- Logs históricos com dados por dia/horário/local.

## 🔁 Interação
- O **Motor de rastreamento** processa os frames ddo video e envia os dados para o **Agente de Análise** em forma Json.
- O **Agente de Análise** gera estatísticas, detecta padrões, etc.
- O **Agente de Relatório** consome essas informações para geração de relatório detalhado.

## 📌 Status Inicial do Projeto
- [x] Ideia discutida e validada com o professor  
- [x] Estrutura básica do repositório criada  
- [x] Quadro no GitHub Projects criado  
- [x] Primeiras tarefas definidas e atribuídas
- [ ] Encapsulamento completo dos scripts como agentes
- [ ]  Integração com LLM e geração de relatório

## 📄 Documentação Futura
Este repositório poderá incluir:
- Relatórios parciais de progresso  
- Scripts de testes ou simulações  
- Resultados e conclusões finais  
- Diagramas de arquitetura do sistema multiagente
