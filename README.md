# Atividade de Inteligência Artificial - Formação Tecnológica 4.0 - COMPET

Atividade proposta pelo professora de Inteligência Artificial. Este repositório contém um projeto classificação da qualidade de vinhos utilizando técnicas de Aprendizado de Máquina. O objetivo é prever a qualidade do vinho (baixa, média ou alta) a partir de características químicas, utilizando Python, pandas, scikit-learn e uma interface interativa com Gradio.

## Estrutura do Projeto

```
.
├── codigo/
│   ├── aplicacao.ipynb         # Interface Gradio para previsão
│   ├── coleta.ipynb            # Coleta, análise e transformação dos dados
│   ├── treinamento.ipynb       # Treinamento e avaliação dos modelos
├── dados/
│   ├── dados_origem.csv        # Dados originais coletados
│   └── dados_transformados.csv # Dados tratados e prontos para modelagem
├── modelo/
│   └── modelo_treinado.pkl     # Modelo treinado salvo (SVC)
├── requirements.txt            # Dependências do projeto
└── README.md                   # Este arquivo
```

## Descrição das Etapas

- **Coleta e Análise dos Dados**  
  Os dados foram obtidos do [Kaggle](https://www.kaggle.com/datasets/sahideseker/wine-quality-classification) e analisados em `codigo/coleta.ipynb`. Foram realizadas análises estatísticas, tratamento de dados e transformação de variáveis categóricas em numéricas.

- **Treinamento dos Modelos**  
  Em `codigo/treinamento.ipynb`, foram treinados dois modelos: RandomForest e SVC. O modelo SVC apresentou melhor desempenho e foi salvo para uso posterior.

- **Aplicação Interativa**  
  O notebook `codigo/aplicacao.ipynb` implementa uma interface gráfica com Gradio, permitindo ao usuário inserir características do vinho e obter a previsão de qualidade.

## Como Executar

1. **Instale as dependências:**
   ```powershell
   pip install -r requirements.txt
   ```

2. **Execute os notebooks na ordem:**
   - `codigo/coleta.ipynb` para preparar os dados.
   - `codigo/treinamento.ipynb` para treinar e salvar o modelo.
   - `codigo/aplicacao.ipynb` para rodar a interface Gradio.

3. **Acesse a interface Gradio:**  
   Após rodar o notebook de aplicação, será exibido um link local para acessar a interface web.

## Tecnologias Utilizadas

- Python 3.11+
- pandas
- numpy
- matplotlib
- scikit-learn
- gradio

## Observações

- Os dados de entrada para previsão devem seguir o padrão das colunas: `acidez_fixa`, `acucar_residual`, `alcool`, `densidade`.
- O modelo prevê a qualidade do vinho como 0 (baixa), 1 (média) ou 2 (alta).

---

**Justificativa da base de dados ou API escolhida.**

A escolha desta base de dados se deu, primeiramente, pelo fato de achá-la bastante interessante, mesmo não sendo apreciador de vinho. Além disso, considerei a base simples e adequada para a proposta de resolver um problema de classificação, permitindo aplicar técnicas de aprendizado de máquina de forma clara e objetiva.