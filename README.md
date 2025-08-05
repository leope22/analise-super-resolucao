# Análise de Super-Resolução de Imagens com Aprendizado Profundo

Análise comparativa do desempenho de modelos de Super-Resolução (SR) baseados em CNNs, GANs e Transformers, avaliando sua robustez e eficácia sob diferentes cenários de degradação de imagem.

## 📜 Sobre o Projeto

O objetivo deste projeto é analisar como diferentes arquiteturas de aprendizado profundo para Super-Resolução de Imagens se comportam quando apresentadas a imagens de baixa resolução com múltiplas e variadas degradações. A investigação aborda modelos "clássicos", treinados para uma degradação específica (bicúbica), e para a análise visual, adiciona modelos de "Super-Resolução Cega" (Blind SR), projetados para lidar com problemas complexos e desconhecidos do mundo real.

A avaliação foi realizada utilizando métricas de fidelidade (PSNR, SSIM, RMSE) e de percepção visual (LPIPS), além de uma análise qualitativa detalhada dos resultados.

## 🤖 Modelos Investigados

Foram selecionados modelos pré-treinados representativos de diferentes abordagens de Super-Resolução.

#### 1\. Modelos de Super-Resolução Clássica

*Treinados primariamente com degradação bicúbica.*

  * **EDSR:** Modelo baseado em CNN (Redes Residuais), otimizado para métricas de fidelidade como o PSNR.
  * **ESRGAN:** Modelo baseado em GAN, focado em gerar resultados visualmente realistas e perceptualmente convincentes.
  * **SwinIR (Clássico):** Modelo baseado em Transformers, que utiliza mecanismos de atenção para capturar dependências de longo alcance na imagem.

#### 2\. Modelos de Super-Resolução Cega (Blind SR)

*Treinados com múltiplas e complexas degradações (borrões, ruídos, compressão JPEG, etc.).*

  * **Real-ESRGAN:** Treinado com um modelo de degradação mais realista.
  * **BSRGAN:** Utiliza um processo de degradação complexo e aleatório.
  * **SwinIR (Real):** Versão do SwinIR que utiliza a metodologia de treinamento do BSRGAN para lidar com degradações do mundo real.

## 🌪️ Degradações Aplicadas

Para testar a robustez dos modelos, as imagens de alta resolução foram submetidas a 9 tipos diferentes de degradação, incluindo:

  * **Métodos de Interpolação:** Nearest-Neighbor, Bilinear, Bicúbica, Lanczos e Hamming.
  * **Degradações Complexas:**
      * Borrão Gaussiano (Gaussian Blur)
      * Borrão de Movimento (Motion Blur)
      * Ruído Gaussiano (Gaussian Noise)
      * Ruído Sal e Pimenta (Salt and Pepper Noise)

## 📄 Visualização do Projeto e Relatório Completo

O código-fonte e os scripts principais estão neste repositório. No entanto, para uma experiência de visualização mais rica, com todas as saídas, gráficos e a documentação detalhada do projeto, utilize os links abaixo:

* **Notebook Interativo (Google Colab):**
    Para visualizar e executar o notebook de forma interativa, com todos os gráficos e resultados da análise, utilize o link do Google Colab.

    **[➡️ Abrir Notebook no Google Colab](https://colab.research.google.com/drive/1tTIcLRLKgSDaLAVgmQ8yFicgkPYZqnWh?usp=sharing)**

* **Relatório Técnico do Projeto (PDF):**
    O artigo completo detalhando a metodologia, os experimentos e as conclusões aprofundadas do projeto está disponível para leitura no Google Drive.

    **[➡️ Ler Relatório Completo](https://drive.google.com/file/d/1otVqIMjMSv1AmK-gBXa4XNwfBRWJ1vb3/view?usp=sharing)**
