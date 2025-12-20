# EfficientEnsemble - Diagnóstico de Câncer de Mama em Ultrassom

## 📌 Visão Geral
Este projeto propõe um método para classificação de câncer de mama em imagens de ultrassom, combinando técnicas de Processamento Digital de Imagens com Deep Learning. O pipeline inclui extração automática da Região de Interesse (ROI) a partir das máscaras do dataset BUSI, seguida de pré-processamento para redução de ruído e realce de estruturas relevantes.

## 🧠 Pré-processamento e Dados
Após a extração da ROI, é aplicado filtro guiado em conjunto com filtro da mediana, e um esquema de aumento de dados direcionado apenas à classe minoritária (malignant), visando reduzir o desbalanceamento do conjunto de treino. O dataset é então dividido de forma estratificada em treino, validação e teste.

## 📊 Modelos e Avaliação
Para a classificação, são treinados três modelos EfficientNet (B0, B1 e B2) com pesos pré-treinados no ImageNet. Os modelos são avaliados individualmente e combinados por meio de um ensemble por votação majoritária, sendo analisados com métricas como acurácia, sensibilidade, especificidade, F1-score e AUC-ROC.

O projeto foi desenvolvido como Trabalho Final da disciplina de Processamento Digital de Imagens.
