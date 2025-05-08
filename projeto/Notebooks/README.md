# Detecção e Contagem de Pessoas em Espaços Públicos

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

## Detecção de Pessoas com YOLO

O notebook [`detectionyolo.ipynb`](detectionyolo.ipynb) demonstra a detecção de pessoas usando YOLOv3 com OpenCV. Ele carrega uma imagem e identifica pessoas com bounding boxes.
- Para ver melhor o resultado recomendo abrir no Colab

## Requisitos
Python 3.7+

OpenCV (opencv-python)

NumPy

Google Colab (ou ambiente com suporte a Jupyter)

Recomenda-se uso de GPU para melhor desempenho.

## 🤖 Agentes Envolvidos
- **Agente de Visão (Detector)**: Responsável por detectar pessoas nas imagens captadas pelas câmeras usando visão computacional.  

## 🧱 Tecnologias Pretendidas
- **Linguagem de Programação:** Python  
  > Escolhida por ser amplamente usada em aplicações de visão computacional e possuir grande variedade de bibliotecas especializadas.

- **Bibliotecas e Frameworks:**
  - **YOLO / OpenCV + Haar Cascades**: Para detecção de pessoas.  
    > YOLO é rápido e eficiente para detecção em tempo real; Haar é uma alternativa mais leve para ambientes com menos poder computacional.

## 📦 Entradas e Saídas Esperadas
**Entradas:**
- Vídeos ou imagens de câmeras em tempo real.

**Saídas:**
- Contagem de pessoas em tempo real.

