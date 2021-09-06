# Redes-Neuronales--Ejercicio
 Primeros pasos con Redes Neuronales. Examinamos un dataset de móviles, donde aparecen las principales características reunidas en 25 variables.
 
 **Importación de datos**
Modificamos los datos de DataFrame a una matriz de numpy

**Preprocesado**
* Deben estar en formato numérico
* Recomendable dentro del rango [0 1] (StandarScale)
* Binarizar las clases (OneHotEncoder)

**Diseño del modelo**
Diseño del modelo con 4 capas ocultas, 20, 45, 10, 20 neuronas. Función de activación 'relu' y función de activación en la capa de salida 'softmax'
 
**Visualizamos**

![image](https://user-images.githubusercontent.com/79086731/132190010-9510bc15-36c6-4cbb-a008-af5935667cce.png)


Este modelo no esta correctamente diseñado, hay un exceso de neuronas en las capas intermediaS, la función de pérdida tiene cuatro clases por lo que no puede ser binary crossentropy, el número de épocas es reducido...

**Regularización**

Utilizaremos regularización para procurar evitar el sobre ajuste del modelo utilizando después de cada capa un Dropout del 40 % de probabilidad de mantener la neurona tras cada capa oculta. 'model4.add(Dropout(0.6))' Utiliza de los modelos anteriores aquel que mayor overfitting presenta.

![image](https://user-images.githubusercontent.com/79086731/132188881-7c311cd0-4e58-48b8-b798-45d1795134c4.png)

