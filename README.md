Se exploraron 2 modelos. Uno probabilistico y un Decision Tree.

Ambos proponen N=5 productos. Para probar el accuracy de los modelos se elige cierta cantidad de clientes y se recomiendan N=5 productos usando la data hasta la anteultima orden. Si los productos están presentes en la última orden entonces el modelo funciona bien.

El modelo probabilistico mostró un accuracy del ~20% y el Decision Tree del ~27%

[Nota] ambos modelos utilizan la información respecto de si los productos son o no pedidos en una orden. No utilizan información del tamaño de los pedidos

### Modelo Probabilistico

Se armaron dos distribuciones de probabilidad para cada producto. Una, la cantidad de ordenes hasta el primer pedido. La segunda, la cantidad de ordenes entre pedidos.

Con estas dos curvas se puede estimar en cualquier momento la probabilidad de que el producto seá pedido en la siguiente orden.

El modelo mostró un accuracy del ~27%.

No se usó datos de los clientes para armar las curvas. Una siguiente mejora podría ser armar las curvas por producto y por tipo de cliente.

Notar que éste modelo no es capaz de estimar interacciones entre productos. Esto podría ser o no ser un limitante.

### Modelo Decision Tree

El modelo mostró un accuracy del 27%.

El modelo utiliza únicamente data del último pedido y el BusinessSegmente al que pertenece el cliente.

Una de las mejoras siguientes debería ser el feature engineering para elegir otras variables que se puedan utilizar. Como datos del cliente, ordenes pasadas y tamaño de los pedidos

Otra mejora que se debe hacer aún es el hyper parameter tunning del arbol.


### Otros modelos

Sería interesante probar un modelo de deep learning con transformers.