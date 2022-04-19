# Análise Exploratória de Pacientes Diabéticos

![iStock-1169420357-2120x1060](https://user-images.githubusercontent.com/96497622/163745289-55c68aac-37b3-4634-87d6-6b492a283ee7.jpg)

## 1. Objetivo

Este projeto faz parte do curso de Análise de Dados com Linguagem Python da [Data Science Academy](https://www.datascienceacademy.com.br/start), e tem o intuito de aplicar técnicas de análise de dados utilizando banco de dados relacional `SQLite`, `Python` e `SQL`.

O objetivo é simular uma necessidade que foi solicitada por uma cientista de dados e entregá-lo uma amostra com os pacientes com mais de 50 anos e, para cada um deles, indicar em uma nova coluna se o paciene está normal ou obeso. Se BMI for menor que 30, o paciente está normal. Se o BMI for maior ou igual a 30, então o paciente está obeso. A partir disso, deverá ser criado um novo arquivo CSV e encaminhar ao cientista de dados.

## 2. Coleta e Extração dos Dados

O dataset utilizado foi obtido da plataforma [Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database) e contém informações do Instituto Nacional de Diabetes e Doenças Digestivas e Renais, dos Estados Unidos. 

O dataset possui 768 registro em 9 colunas e contém dados de mulheres a partir de 21 anos de idade do povo indígena americano Pima.

| Atributo | Tipo | Descrição |
|--- |--- |--- |
| Pregnancies | INT | Quantas vezes engravidou
| Glucose | INT | Concentração de glicose plasmática em um teste oral de tolerância à glicose
| BloodPressure | INT | Pressão arterial diastólica (mm Hg)
| SkinThickness | INT | Espessura da dobra cutânea do tríceps (mm)
| Insulin | INT | Insulina sérica de 2 horas (mu U/ml)
| BMI | DECIMAL(8,2) | IMC - Índice de massa corporal (peso em kg/altura em m²)
| DiabetesPedigreeFunction | DECIMAL(8,2) | Função hereditária do diabetes
| Age | INT | Idade (anos)
| Outcome | INT | Indica se teve ou não diabetes (0: não teve diabetes / 1: teve diabetes) 

## 3. Ferramentas

Foi utilizado o aplicativo web open-source `Jupyter Notebook`. Foram instalados os pacotes Watermark (para gravar as versões de outros pacotes usados no Jupyter Notebook utilizado) e ipython-SQL (para rodar instruções SQL no Jupyter Notebook) e importados os pacotes `Pandas` e `SQLite3`.

## 4. Técnicas de Análise

Foram utilizadas técnicas de exploração dos dados para agregação e sumarização dos registros, para atender o objetivo do projeto e realizadas as seguintes etapas:

1. Carregar o dataset original ('diabetes.csv') em um dataframe do Pandas
2. Copiar este dataframe para dentro do banco de dados SQLite como uma tabela ('diabetes.csv')
    1. Criar uma tabela ('pacientes.csv') vazia no banco de dados
    2. Inserir os registros de 'diabetes.csv' para 'pacientes.csv' onde a idade for maior que 50 anos
    3. Criar a coluna 'Perfil' em 'pacientes.csv' e aplicar regra da condição BMI para saber se o paciente está normal ou obeso
3. Carregar os dados no Pandas e salvar como .CSV

## 5. Resultados

O dataframe resultante possui 81 registros e 10 colunas.

<!--- Comentários - Plano de análise de dados

1. Definição do objetivo (O que queremos analisar? Quais perguntas devem ser respondidas?)
2. Coleta e extração dos dados
3. Escolha das ferramentas
4. Aplicação das técnicas de análise (análise exploratória, estatística descritiva, agregação, sumarização, estatística inferencial, mineração de dados, ML etc.)
5. Entrega dos resultados (relatórios, gráficos, tabelas, etc.)
-->


