# Detecção de Falhas em Rolamentos com IA (NASA Dataset) 🏎️⚙️

Projeto de Manutenção Preditiva desenvolvido para aplicação em sistemas rotativos (Baja SAE / Indústria). O objetivo é prever falhas catastróficas antes que elas ocorram usando análise de vibração e Machine Learning não-supervisionado.

## 🎯 Resultados
- **Modelo Escolhido:** K-Means (Clustering).
- **Performance:** 100% de detecção de falhas (Recall) e zero falsos negativos.
- **Hardware:** Modelo otimizado para rodar em microcontroladores (ESP32/Arduino) através de coeficientes de distância euclidiana.

## 🛠️ Tecnologias
- Python (Pandas, Scikit-Learn, SciPy)
- Processamento de Sinais (RMS, Curtose, FFT)
- Análise de Dados da NASA (IMS Bearing Dataset)

## 📊 Metodologia
1. **Coleta:** Leitura de arquivos brutos de vibração (20kHz).
2. **Feature Engineering:** Extração de indicadores físicos. Descobrimos que a **Curtose** antecipa a falha dias antes do RMS subir.
3. **Modelagem:** Treinamento de K-Means apenas com dados saudáveis (Detecção de Anomalias).
4. **Deploy:** Extração de limiares para implementação embarcada.
