# Clasificacion Automatica de Tickets con NLP

Integrantes

Wilder Serdan (wserdan@gmail.com)
Oscar Ramirez (oscar.ramirez.guachalla@gmail.com)
Ruth Daniela Villalobos (ruthdanivillalobos@gmail.com)

## Table of Contents

1. Setup e Importación de Librerias
2. Data Loading
3. Text preprocessing
4. Exploratory Data Analysis (EDA)
5. Feature Extraction
6. Topic modeling 
7. Model building using Supervised Learning
8. Model training and evaluation
9. Model inference

#Introduction

El proyecto consta de un clasificador de quejas de clientes en función de los productos/servicios. 
Segregando estos tickets en sus categorías relevantes y por lo tanto, ayudar en la resolución rápida del problema.

#Methods Used
Realizar el estudio del contenido de las quejas realizar el tratamiento con las librerias nltk y spacy para posteriormente
clasificarlo con los modelos: 
*Logistic regression
*Decision Tree
*Random Forest
*Naive Bayes

##Importación de Librerias
json
numpy
pandas
re
nltk
spacy
seaborn
matplotlib
plotly


#Download and Setup
Prerequisitos
Para lograr ver los resultados de este proyecto, se recomienda el uso de un Jupyter Notebook, en este caso se hizo uso de Google Colab Notebooks, los cuales vienen enlazados con una cuenta de gmail y no es necesario otro requisito para su uso.

Sin embargo, puede lograrse un normal funcionamiento con una instalación de Python y el uso de cualquier herramienta de edición (en algunos casos puede requerir la instalación de algunas librerias extra).

#How to Run
Se puede hacer uso de este proyecto con el siguiente procedimiento:

Clonar el repositorio desde GitHub
Copiar en url del repo y en una terminal de su preferencia seguir estos pasos:
Ubicar una carpeta para almacenar el proyecto
Escribir en la terminal: git clone
Abrir el archivo .ipynb y verificar que la base de datos este bien ruteada.
Empezar a correr los pasos propuestos.
Copiar el contenido en un Google Colab Notebook, verificando que la base de datos tambien se encuentren ahi.


#Most Significant Variables are:

*Logistic regression   Score=0.904

                                            precision    recall  f1-score   support

            Servicios de Cuentas de Banco       0.88      0.95      0.91      1287
Tarjetas de Credito / Tarjetas Prepagadas       0.92      0.91      0.91      1326
                                    Otros       0.95      0.81      0.87       568
                        Reportes de Robos       0.89      0.90      0.89      1075
         Ptmos Hipotecarios y Otros Ptmos       0.92      0.91      0.91      1012

                                 accuracy                           0.90      5268
                                macro avg       0.91      0.89      0.90      5268
                             weighted avg       0.91      0.90      0.90      5268
							 

*Decision Tree		 Score=0.783			
								             precision    recall  f1-score   support

            Servicios de Cuentas de Banco       0.79      0.80      0.80      1565
Tarjetas de Credito / Tarjetas Prepagadas       0.81      0.82      0.81      1546
                                    Otros       0.74      0.74      0.74       674
                        Reportes de Robos       0.76      0.75      0.75      1321
         Ptmos Hipotecarios y Otros Ptmos       0.79      0.78      0.79      1216

                                 accuracy                           0.78      6322
                                macro avg       0.78      0.78      0.78      6322
                             weighted avg       0.78      0.78      0.78      6322

*Random Forest        Score=0.808		 

                                              precision    recall  f1-score   support

            Servicios de Cuentas de Banco       0.76      0.92      0.83      1565
Tarjetas de Credito / Tarjetas Prepagadas       0.80      0.87      0.83      1546
                                    Otros       0.94      0.43      0.59       674
                        Reportes de Robos       0.82      0.79      0.81      1321
         Ptmos Hipotecarios y Otros Ptmos       0.86      0.81      0.83      1216

                                 accuracy                           0.81      6322
                                macro avg       0.84      0.77      0.78      6322
                             weighted avg       0.82      0.81      0.80      6322
							 
							 
*Naive Bayes          Score=0.692

                                              precision    recall  f1-score   support

            Servicios de Cuentas de Banco       0.60      0.93      0.73      1565
Tarjetas de Credito / Tarjetas Prepagadas       0.68      0.78      0.72      1546
                                    Otros       1.00      0.00      0.01       674
                        Reportes de Robos       0.81      0.64      0.72      1321
         Ptmos Hipotecarios y Otros Ptmos       0.81      0.72      0.76      1216

                                 accuracy                           0.69      6322
                                macro avg       0.78      0.61      0.59      6322
                             weighted avg       0.75      0.69      0.65      6322


El mejor clasificador es logistic regresion debido que tiene un score de 0.904 
adicionalmente las caracteristicas de presision son mas altas en comparacion a las 
variaciones de los otros modelos.

