# 🔨 Análise de Score de Clientes

Este projeto tem como objetivo analisar o **score de crédito** de clientes utilizando dois modelos de **Inteligência Artificial (IA)**: Random Forest e K-Nearest Neighbors (KNN). Ambos os modelos são treinados com dados históricos e utilizados para prever a classificação de score de crédito de novos clientes.

## 📈 Sobre o Score de Crédito
O score de crédito dos clientes será classificado em três categorias:
- **😎 Good**: Bom
- **😐 Standard**: Ok
- **🙁 Poor**: Ruim

## 🔄 Funcionalidades do Projeto
1. **🔢 Treinamento de Modelos:**
   - Treinamento dos modelos Random Forest e KNN com dados históricos ajustados.
2. **⚖️ Avaliação de Desempenho:**
   - Cálculo da acurácia para avaliar qual modelo apresenta o melhor desempenho.
3. **🔢 Previsão de Score de Novos Clientes:**
   - Utiliza o modelo mais preciso (Random Forest) para prever o score de crédito de novos clientes.

## 🌐 Etapas do Projeto

### 1. 🔠 Importação das Bibliotecas
As seguintes bibliotecas serão utilizadas no projeto:
- **Pandas**: Para manipulação e análise de dados.
- **Scikit-learn**: Para:
  - Ajuste dos dados (LabelEncoder);
  - Divisão entre dados de treino e teste (train_test_split);
  - Treinamento e avaliação de modelos (RandomForestClassifier e KNeighborsClassifier);
  - Cálculo de acurácia (accuracy_score).

### 2. ⚙️ Ajuste da Base de Dados
- A base de dados original contém colunas com valores em texto (strings). Essas colunas são convertidas para valores numéricos utilizando o **LabelEncoder**.
- A coluna **score_credito** é a variável dependente (*target*), enquanto as demais colunas (exceto **id_cliente**) são as variáveis independentes (*features*).

### 3. 🧬 Treinamento dos Modelos
- Dois modelos são criados e treinados:
  - **Random Forest**:
    - Modelo baseado em árvores de decisão.
    - Funciona criando várias árvores de decisão em subconjuntos aleatórios dos dados e combinando seus resultados para melhorar a precisão e evitar overfitting.
    - Ideal para problemas de classificação e regressão devido à sua robustez e capacidade de lidar com grandes conjuntos de dados.

  - **K-Nearest Neighbors (KNN)**:
    - Modelo baseado em proximidade.
    - Funciona encontrando os "K" exemplos mais próximos no conjunto de dados de treino para cada ponto a ser classificado, baseando a previsão na maioria das classes desses vizinhos.
    - Simples, mas eficaz para conjuntos de dados menores e menos complexos.

- Os dados são divididos em conjunto de treino (70%) e teste (30%) para avaliar o desempenho.

### 4. 🔬 Avaliação de Desempenho
- As previsões realizadas pelos dois modelos são comparadas com os valores reais.
- A acurácia de cada modelo é calculada utilizando a função **accuracy_score**.
- O modelo com melhor desempenho é selecionado para previsões futuras (neste caso, o **Random Forest**).

### 5. 🔶 Previsão de Novos Clientes
- Uma nova base de dados contendo informações de novos clientes é importada.
- Os mesmos ajustes realizados na base de treino são aplicados na nova base.
- O modelo **Random Forest** é utilizado para prever o score de crédito desses clientes.

## 🔧 Como Executar o Projeto

1. **Faça o clone do projeto**
      ```git
      git clone https://github.com/Robert-Cortez-Rudi/Score_clientes_IA
      ```

2. **Instale as dependências:**
   - Certifique-se de ter o Python instalado.
   - Instale as bibliotecas necessárias:
     ```bash
     pip install requirements.txt
     ```

3. **Prepare os dados:**
   - Certifique-se de que o arquivo `clients.csv` (base de treino) e `new_clients.csv` (novos clientes) estão na mesma pasta do script.

4. **Execute o projeto:**
   - O projeto deve ser executado em um arquivo **Jupyter Notebook (.ipynb)**. Certifique-se de ter o Jupyter instalado nas extensões.
   - Abra o Jupyter e execute as células sequencialmente para treinar os modelos e prever o score de novos clientes.

## 🎯 Resultados Esperados
- Um modelo treinado com alta acurácia para previsão de score de crédito.
- Previsões de score de crédito para novos clientes.

## 🌐 Tecnologias Utilizadas
- Linguagem: **Python**
- Ferramenta: **Jupyter Notebook**
- Bibliotecas:
  - **Pandas**
  - **Scikit-learn**

---

Este projeto foi desenvolvido com a função de aplicar técnicas de machine learning na classificação de dados e pode ser utilizado como base para soluções semelhantes no mercado financeiro. 🌟

