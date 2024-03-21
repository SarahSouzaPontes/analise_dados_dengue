1.Arquivo ( análise de estatística descritiva das variáveis) Análise de Dados - Temática Dengue.pdf 


2.Arquivo ( script em Python) CIDACS.ipynb


3.Arquivo ( dicionário online) DIC_DADOS_ONLINE.pdf


4.Arquivo ( nota informativa pública do formulário de coleta) Nota_Informativa_059.pdf


5.Arquivo ( relatório automatizado pandas compactado) Relatório Base de Dados HTML.zip


6.Arquivo ( script Python em PDF) SCRIPT_CIDACS.ipynb - Colaboratory.pdf


7.Arquivo ( pasta compactada dos arquivos iniciais) selecao-curadoria-main.zip# analise_dados_dengue

8. Arquivo ( script em Python) Qualidade_dos_Dados_pynb

9. Arquivo ( em pdf) Relatório da Qualidade_dos_Dados_pdf

10. Arquivo ( em pdf & Python) com a referência da Semana Epidemiológica (http://www.portalsinan.saude.gov.br/calendario-epidemiologico-2013 / SINANWEB - Calendário Epidemiológico 2013.pdf) realizei o script para a conferência dos dados -> SCRIPT_CONFERÊNCIA_DA_SEMANA_EPIDEMIOLÓGICA_AUXÍLIO_AO_DICIONÁRIO_DE_DADOS.ipynb

11. Arquivo ( em pdf ) Adicional.pdf a avaliação qualidade dos dados.

12. Arquivo ( em pdf ) Dicionário de Dados - BCO Dengue.pdf

13. Arquivo ( em jpg ) Fluxograma das atividades realizadas



![Dicionário de Dados, Análise da Qualidade dos Dados, Análise dos Dados, Balanceamento, Modelagem, Relatórios](URL_DA_IMAGEM)
![Logo do GitHub](https://github.com/SarahSouzaPontes/analise_dados_dengue/blob/main/Fluxograma.jpg)





Alguns materiais de apoio:

1.https://medium.com/@danielly.bx/tutorial-diagrama-de-controle-epidemiol%C3%B3gico-no-r-6633981ba34f
2.https://opendatasus.saude.gov.br/
3.https://portal.fiocruz.br/doenca/dengue
4.https://portalsinan.saude.gov.br/sinan-dengue-chikungunya
















                    VERDADEIROS NEGATIVOS   FALSO POSITIVOS

                 |   Previsto Negativo   |   Previsto Positivo   |

Negativo (0) |         7707          |           0           |

Positivo (1) |           7           |           0           |
                FALSO NEGATIVOS         VERDADEIROS POSITIVOS

Verdadeiros Negativos (TN): São os exemplos que foram corretamente classificados como negativos pelo modelo. No caso fornecido, há 7707 verdadeiros negativos.

Falsos Positivos (FP): São os exemplos que foram incorretamente classificados como positivos pelo modelo, quando na verdade são negativos. No caso fornecido, não há falsos positivos (valor = 0).

Falsos Negativos (FN): São os exemplos que foram incorretamente classificados como negativos pelo modelo, quando na verdade são positivos. No caso fornecido, há 7 falsos negativos.

Verdadeiros Positivos (TP): São os exemplos que foram corretamente classificados como positivos pelo modelo. No caso fornecido, não há verdadeiros positivos (valor = 0).

Precisão (Precision):

A precisão é a proporção de exemplos positivos previstos corretamente em relação ao total de exemplos previstos como positivos pelo modelo. Neste caso, a precisão para a classe 0 é 1.00, o que significa que todos os exemplos previstos como classe 0 foram corretamente classificados. Para a classe 1, a precisão é 0.00, indicando que nenhum exemplo previsto como classe 1 foi corretamente classificado. Em geral, a precisão é uma medida de quão precisas são as previsões positivas do modelo.

Recall (Recuperação):

O recall, também conhecido como sensibilidade, é a proporção de exemplos positivos reais que foram corretamente identificados pelo modelo. Neste caso, o recall para a classe 0 é 1.00, o que significa que todos os exemplos da classe 0 foram corretamente identificados. Para a classe 1, o recall é 0.00, indicando que nenhum exemplo da classe 1 foi corretamente identificado. Em geral, o recall é uma medida de quão bem o modelo "lembra" dos exemplos positivos.

F1-Score:

O F1-Score é a média harmônica entre precisão e recall e fornece uma única métrica que combina essas duas medidas. Neste caso, o F1-Score para a classe 0 é 1.00, pois a precisão e o recall são ambos 1.00. Para a classe 1, o F1-Score é 0.00, devido à precisão e ao recall serem ambos 0.00. O F1-Score é útil para equilibrar a importância da precisão e do recall em um único valor.

------------------------------------------------------------------------------------------------------------------------------------------------------------
------ R E S O L U Ç Ã O       P A R A            M E L H O R A R            O           M O D E L O -------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------

Lidar com classes desbalanceadas:

Utilize técnicas de balanceamento de classes, como oversampling ou undersampling, antes de dividir os dados em conjuntos de treinamento e teste. Por exemplo, você pode usar a biblioteca imbalanced-learn para aplicar essas técnicas.

Explorar diferentes algoritmos de classificação:

Além da regressão logística, inicialize e treine outros modelos de classificação, como árvores de decisão, florestas aleatórias, SVMs, etc. Você pode criar uma lista de modelos e iterar sobre eles para treinar e avaliar cada modelo individualmente.

Ajustar hiperparâmetros do modelo:

Utilize a busca de hiperparâmetros (por exemplo, utilizando GridSearchCV ou RandomizedSearchCV do scikit-learn) para encontrar a combinação ideal de hiperparâmetros para cada modelo. 

Realizar uma análise mais detalhada das características:

Explore e pré-processe as características do conjunto de dados de forma mais detalhada. Isso pode envolver a remoção de características irrelevantes, tratamento de valores ausentes, normalização de características, entre outras técnicas.

Avaliar métricas adicionais:

Além da acurácia, calcule métricas como precisão, recall, F1-Score e especificidade para cada modelo. Isso pode ser feito utilizando a função classification_report do scikit-learn.


Explorar métodos de validação cruzada:

Utilize métodos de validação cruzada, como k-fold cross-validation, para avaliar o desempenho do modelo de forma mais robusta. Você pode usar a função cross_val_score do scikit-learn para isso.

