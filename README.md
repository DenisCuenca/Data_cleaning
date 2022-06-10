# Data_cleaning
Proceso para limpieza de datos:

Conceptos previos:

    - Limpieza de datos: la  limpieza de datos es el acto de exploración, corrección o eliminación de los reguistros erroneos de una base de datos.
    - Outliers: observación se dista del flujo regular de los datos dentro de un conjunto, de allí que se los conozca como valores atípicos, estos pueden afectar en gran medida la estimación de los datos.



En el presente repositorio se presenta el proceso de limpieza de tres datasets extraidos desde kanggle para análisis financiero:

datos extraidos desde:

    https://www.kaggle.com/code/paulinan/bank-customer-segmentation/data
    https://www.kaggle.com/datasets/sidharth178/customer-segmentation
    https://www.kaggle.com/datasets/shivamb/bank-customer-segmentation



Proceso para limpieza de datasets:
(la ejecución de cada paso se muestra en el notebook  'limpieza_datos')


1. Se importan las libreria a utilizar para la exploracion y manipulación de datos:

 Importar librerias necesarias (en escenario se usó exclusivamente pandas).
 configurar pandas para que muestre todas las columnas del dataset.
 Lectura de archivos a procesar.

 Proceso para limpieza de bank_transactions Dataset

     Conteo de datos datos nulos en cada columna del dataset bank_transactions:

         CustomerDOB                3397    
         CustGender                 1100    
         CustLocation                151    
         CustAccountBalance         2369    


     -- Eliminar nulos -

     Se descartan las columnas con datos nulos: 
        Para ello se crea un nuevo dataframe con las columnas sin valores nulos.
     Verificación de outliers en columnas con valores categórico.
     Corrección de valor mal ingresado para 'CustGender'
         Se remplazo 'T' por el valor con mayor incidencia en la columna ('M').
     Data set Limpio!

     Tras este proceso se pierden 6953 filas del dataset.



    Proceso para limpieza de customer_segmentation dataset


     Conteo de valores nulos en las columnas del dataset
     Remplazo de valores nulos en la columna 'Defaulted' por el valor 0.0
     Conteo de valores nulos
     dataset limpio!




    Proceso para limpieza de german_credit dataset

     Conteo de valores nulos en el dataset
     Conteo de valores categoricos en la columna 'Saving accounts'
     Conteo de valores categoricos en la columna 'Checking account'
     Remplazo de los valores nulos en las columnas 'Checking account' y 'Saving accounts'
     por el valor 'None'
     dataset limpio!


    Exportación de datos procesados:

    los datos limpios se encuestran en la carpeta: data/datos_limpios


fuentes y recusos complementarios:

    https://pandas.pydata.org/docs/
    https://blog.hubspot.es/marketing/limpieza-de-datos
    https://www.youtube.com/watch?v=qxpKCBV60U4&t=721s



