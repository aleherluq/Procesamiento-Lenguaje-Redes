# Redes Neuronales Convolucionales (CNN)

Tipo de red con aprendizaje **supervisado** que procesa sus capas imitando al cortex visual del ojo humano para identificar distintas características en las entreadas que en definitiva hacen que pueda identificar objetos y <<ver>>. Para ello una CNN contiene varias capas ocultas especializadas y con una jerarquía: esto significa que las primeras capas pueden detectar líneas, curvas y se van especializando hasta llegar a capas más profundas que reconocen formas complejas, como un rostro o la silueta de un animal.

Las neuronas convolucionales van avanzando por el vector teniendo en cuenta los componentes que rodean a cada componente.


La función de activación más usada por este tipo de redes es la llamada **ReLu** por Rectifier Linear Unit y consiste en f(x)=max(0,x) 

Se suele utilizar un subsampling para reducir el tamaño de la muestra

La capa de convolución suele procesar la salida de neuronas que están conectadas en "regiones locales" de entrada, es decir, los valores cercanos, calculando el producto escalar entre sus pesos (valor de una palabra concreta) y una pequeña región a la que están conectados el volumen de entrada. 


# Capa Convolucional 1D

`
keras.layers.Conv1D(filters, kernel_size, strides=1, padding='valid', data_format='channels_last', dilation_rate=1, activation=None, use_bias=True, kernel_initializer='glorot_uniform', bias_initializer='zeros', kernel_regularizer=None, bias_regularizer=None, activity_regularizer=None, kernel_constraint=None, bias_constraint=None)
`

Esta capa crea un kernel convolucional que utiliza los datos de entrada para convolucionar sobre una dimensión espacial (o temporal) para producir un tensor de salida. -*use_bias*_ se establece como **True** se crea y se enlaza un vector de bias y se añade a la salida. Por último, si la **activation** se establece como no nula **(!= None)**, se aplica a la salida también.

Cuando se usa esta capa como la primera capa de un modelo, se le porporciona un -*input_shape*_ 

### Argumentos


* **filters**: Entero, la dimensionaldad del espacio a la salida 
* **kernel_size:** Entero o tupla/lista de enteros solitarios, especificando la longitud de la ventana convolucional de 1D
* **strides:** Entero o tupla/lista de enteros, especificando el avance de las convoluciones. Especificar el valor de cualquier paso como != 1 es incomplatible con especificar **dilation_rate** con valor !=1
* **padding:** Existen varios casos: **valid**, que significa que no hay padding. **same**  el padding resultante hace que la entrada tenga la misma longitud que la salida. **"casual"** esta resulta en convoluciones "casual", por ejemplo en el caso de que la salida de una no dependa de la entrada de la siguiente.
* ****
* ****
* ****