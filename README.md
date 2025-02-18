<h1 align="center" font-size="200em"><b>Análise de Sensores com Machine Learning</b></h1>
<div align = "center" >
<!-- imagem -->

[![requirement](https://img.shields.io/badge/IDE-Visual%20Studio%20Code-informational)](https://code.visualstudio.com/docs/?dv=linux64_deb)
![Linguagem](https://img.shields.io/badge/Linguagem-python-orange)
</div>

## 📌 Descrição do Projeto
Este projeto tem como objetivo analisar dados de sensores, tratando valores ausentes (NaN) e avaliando como isso afeta a performance de modelos de Machine Learning. Foram utilizados os algoritmos **Random Forest** e **Gradient Boosted Trees (GBT)** para realizar a classificação e comparar os resultados entre diferentes abordagens de tratamento de dados.

## 🔧 Tratamento de Dados
Os dados passaram por duas abordagens distintas para lidar com valores ausentes:
1. **Substituição dos valores NaN pela média da coluna**, permitindo manter o máximo de informações possíveis no conjunto de dados.
2. **Remoção das linhas contendo valores NaN**, reduzindo a quantidade de dados utilizados no treinamento do modelo, mas garantindo que apenas informações completas fossem utilizadas.

## 📊 Resultados e Impacto
Quando utilizamos a substituição dos valores NaN pela média da coluna, o modelo GBT apresentou um **recall de 1.00 para a classe majoritária e 0.95 para a classe minoritária**. O recall mede a capacidade do modelo de identificar corretamente os casos positivos. Como os sensores podem lidar com situações onde dados ausentes são comuns, essa abordagem permitiu que o modelo preservasse melhor o padrão dos dados e fizesse previsões mais confiáveis.

Já na abordagem em que removemos todas as linhas contendo valores NaN, o recall para a classe minoritária caiu para **0.82**, indicando que o modelo teve mais dificuldade em identificar corretamente esses casos. Isso pode ter ocorrido porque a remoção das linhas reduziu drasticamente a quantidade de dados disponíveis para treinamento, diminuindo a capacidade do modelo de aprender padrões relevantes.

O **F1-score**, que é uma métrica que combina precisão e recall para avaliar o desempenho geral do modelo, também foi afetado. Quando utilizamos a média para preencher os valores ausentes, o F1-score se manteve próximo de **0.97** na média, enquanto ao remover as linhas com NaN, ele caiu para **0.91**. Isso mostra que o modelo treinado com substituição de valores ausentes conseguiu um desempenho mais equilibrado, enquanto a remoção dos dados resultou em uma perda de informações que comprometeu a capacidade preditiva do modelo.

## 📉 Impacto da Remoção dos Dados NaN
O total de linhas no conjunto de dados antes do tratamento era **220320**. Após a remoção das linhas com valores NaN, restaram apenas **119103**, representando uma **redução de aproximadamente 45.9%** dos dados. Essa redução significativa afetou diretamente o desempenho dos modelos, pois menos dados significam menos exemplos para o aprendizado, o que pode levar a um modelo menos robusto e com menor generalização.

Essa diferença de desempenho mostra que, em muitos casos, **é mais vantajoso aplicar técnicas de imputação de dados (como substituir por média) ao invés de simplesmente remover dados incompletos**. Isso é especialmente importante em aplicações como sensores, onde a perda de dados pode ser frequente e a reconstrução de padrões pode ajudar na tomada de decisão.

## ✅ Conclusão
Os experimentos realizados demonstraram que o tratamento de dados ausentes é um fator crítico para a qualidade dos modelos de Machine Learning. Substituir valores ausentes pela média manteve um volume maior de dados para treinamento e permitiu que o modelo tivesse um desempenho melhor. Por outro lado, remover dados ausentes resultou em uma amostra menor e, consequentemente, um modelo com recall reduzido e um F1-score inferior, impactando sua capacidade preditiva.


---
## 🗂️Referências
- https://medium.com/gbtech/modelos-de-machine-learning-uma-compara%C3%A7%C3%A3o-entre-os-modelos-parte-2-3b79cd2c84ab
- https://www.escoladnc.com.br/blog/analise-comparativa-de-modelos-de-machine-learning-para-previsao-de-precos-de-imoveis/

## 👾Compilação e execução
* Especificações da máquina em que o código foi rodado:
  * Processador Intel Core i7, 12th Gen;
  * Sistema Operacional Ubuntu 22.04.5;
  * 16GB de RAM.
* | Comando                |  Função                                                                                           |                     
  | -----------------------| ------------------------------------------------------------------------------------------------- |
  |  `make clean`          | Apaga a última compilação realizada contida na pasta build                                        |
  |  `make`                | Executa a compilação do programa utilizando o gcc, e o resultado vai para a pasta build           |
  |  `make run`            | Executa o programa da pasta build após a realização da compilação                                 |



## ✉️Contato
<div>
 <p align="justify"> Jullia Fernandes Felizardo</p>
 <a href="https://t.me/JulliaFernandes">
 <img align="center" src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/> 
 </div>
<a style="color:black" href="mailto:julliacefet@gmail.com?subject=[GitHub]%20Source%20Dynamic%20Lists">
✉️ <i>julliacefet@gmail.com</i>
</a>
