# Classificação de Imagens com Rede Neural Convolucional (CNN) - MNIST 🤖

Este projeto implementa um modelo de rede neural convolucional (CNN) para classificar imagens de dígitos manuscritos da base de dados MNIST. O modelo é treinado, avaliado e gerado com métricas como **Acurácia**, **Sensibilidade**, **F1-Score** e a **Curva ROC** para análise do desempenho do modelo. 📊

## Funcionalidades 🚀

- **Treinamento**: O modelo é treinado usando a base de dados MNIST.
- **Métricas**: Cálculo de **Sensibilidade**, **Precisão**, **F1-Score** e **Acurácia**.
- **Matriz de Confusão**: Exibição da matriz de confusão normalizada para visualização do desempenho do modelo.
- **Curva ROC**: Geração da curva ROC para avaliar a performance do modelo com diferentes limiares.

## Estrutura do Código 📝

O código é dividido em várias seções:

1. **Importação de Bibliotecas**: O código começa com a importação das bibliotecas necessárias, incluindo **TensorFlow**, **NumPy**, **Seaborn**, **Pandas**, **Matplotlib** e **Scikit-learn**.

2. **Carregamento e Pré-processamento dos Dados**:
   - O conjunto de dados **MNIST** é carregado e pré-processado.
   - As imagens são normalizadas para valores entre 0 e 1.
   - As imagens são reorganizadas para o formato adequado para a rede convolucional.

3. **Definição do Modelo CNN**:
   - O modelo **CNN** é construído com três camadas convolucionais (`Conv2D`) e camadas de pooling (`MaxPooling2D`).
   - As camadas convolucionais ajudam a extrair características espaciais das imagens.
   - A camada **densa** (`Dense`) na parte final da rede faz a classificação, com **10 unidades** (uma para cada dígito de 0 a 9).

4. **Treinamento do Modelo**:
   - O modelo é compilado usando o otimizador **Adam** e a função de perda **sparse_categorical_crossentropy**.
   - O treinamento é realizado por **5 épocas**.

5. **Avaliação e Métricas**:
   - Após o treinamento, o modelo é avaliado usando a base de dados de teste.
   - A **matriz de confusão** é gerada para comparar os valores reais com as previsões.
   - **Sensibilidade**, **Precisão**, **F1-Score** e **Acurácia** são calculados para cada classe.
   - A **curva ROC** é gerada e exibida para visualizar a performance do modelo. 📈
