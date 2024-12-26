# Melhorando o desempenho com xgboost

Vamos aplicar a biblioteca XGBoost em problemas de classificação. Vamos trabalhar com dados da área médica, atuando como cientistas de dados de um grupo de pesquisa que deseja criar um modelo para classificar pacientes como portadores ou não de uma doença cardíaca. Faremos validação cruzada, usaremos técnicas específicas da biblioteca XGBoost, realizaremos ajustes de hiperparâmetros e também trabalharemos com a biblioteca dentro de uma pipeline.

Os dados foram obtidos do UCI Machine Learning Repository. Esses dados foram doados em 1988 e provêm dos resultados clínicos e de testes não invasivos realizados em pacientes submetidos a exames na Cleveland Clinic em Cleveland (Ohio), no Instituto Húngaro de Cardiologia em Budapeste, em um Centro Médico em Long Beach (Califórnia), e também em pacientes de Hospitais universitários em Zurique e Basel (Suíça).

[Dados](https://archive.ics.uci.edu/dataset/45/heart+disease)

Temos na primeira coluna a idade de cada um deles. Temos na segunda coluna o sexo biológico. E aqui nesse caso, quando o valor é igual a 1, é porque é o sexo biológico masculino. E quando é 0, é o sexo biológico feminino.

Na terceira coluna, temos o tipo de dor. Então, eles criaram uma escala que está indo de 1 até 4, que indica o tipo de dor no peito que essa pessoa está sentindo, que é algo que é característico de quem tem uma doença cardíaca. Em seguida, temos a pressão arterial de cada pessoa. Então, começamos aqueles exames médicos que comentei. Temos essa pressão arterial. Também temos o colesterol. Como está o nível de colesterol ali no sangue da pessoa.

Também temos o resultado da glicemia em jejum maior que 120. O que isso quer dizer? Quando está marcado com 0, é porque o valor da glicemia ali, da glicose em jejum da pessoa, não está maior que 120. E quando está maior que 120, o valor na tabela vai ser 1.

Temos depois, os resultados de eletrocardiograma. Então, é muito comum quando a pessoa tem ali a suspeita de uma doença cardíaca, fazer esse tipo de exame para analisar como estão os batimentos cardíacos.

Depois, temos os resultados de ECG, que temos os valores numéricos. Temos também a frequência cardíaca máxima de cada pessoa. E também temos uma coluna sobre dor no exercício. Nesse caso, essa pessoa fez o exercício e se ela sentiu dor, vai ter um valor igual a 1 atribuído nessa coluna. E se o valor for igual a 0, é porque a pessoa não teve dor no exercício.

Temos alguns resultados aqui de depressão ST e inclinação ST, que também são dados de eletrocardiogramas. Então, são resultados específicos para esse tipo de exame. Temos, então, valores numéricos para isso.

Também temos o resultado de número vasos fluro. Isso aqui, nesse caso, é um teste que é feito para verificar a coloração de vasos sanguíneos. É um exame específico para fazer isso. Temos valores numéricos também, como é possível observar. E temos aqui, por exemplo, um tal de teste de cintilografia, que também é um teste específico para verificar como estão os músculos do coração, onde temos também alguns valores numéricos.

E, por fim, temos a nossa coluna alvo, que é o nosso target, que é a doença cardíaca. Então, quando está marcado "Presença", é porque a pessoa tem doença cardíaca. Quando está marcado "Ausência", é porque a pessoa não tem.
