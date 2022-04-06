# macowins

## Requerimientos

- El sistema debera permitir al cliente consultar los tipos de prendas que se venden. Los tipos de prenda son sacos, pantalones y camisas.
- El sistema debera permitir al cliente consultar el precio de cada prenda. El precio dependera del estado de dicha prenda:
	- Nueva: _precioPrenda = precioBase_
	- Promocion: _precioPrenda = precioBase - valorDto_
	- Liquidacion: _precioPrenda = precioBase * 0.5_
- El sistema debera registrar en cada venta las prendas vendidas, su cantidad y fecha en la que se concreto la venta.
- El sistema debera permitir pagos tanto en efectivo como con tarjeta.
- El sistema debera calcular el precio final cuando se pague con tarjeta. El racargo se realiza en funcion de la cantidad de cuotas (cantidadCuotas), un coeficiente de recargo (coeficienteRecargo) y el precio de la prenda teniendo en cuenta su estado (precioPrenda). El precio final sigue esta ecuacion:
_cantidadCuotas * coeficienteRecargo + 0.01 * precioPrenda + precioPrenda_

### **NOTA**: Anote solo los requisitos funcionales que aparecen en el texto. Probablemente existan otros requisitos funcionales y no funcionales que faltarian contemplar pero a falta de contexto no los anoto.