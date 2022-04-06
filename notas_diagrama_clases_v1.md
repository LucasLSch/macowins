# DIAGRAMA DE CLASES VERSION 1

## Razon de descarte

Al elegir herencia para modelar los estados de las prendas se genera el problema de un posible cambio de estado de las prendas. Si una prenda nueva pasa a estar en liquidacion o promocion la instancia de prendaNueva deberia eliminarse de todo registro que se utilice en ese momento y ademas agregar una nueva instancia de prendaLiquidacion o prendaPromocion.