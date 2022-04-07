# DIAGRAMA DE CLASES VERSION 3

Esta version soluciona problemas de la anterior y agrega el requerimiento faltante

## Arreglos

- Nombres mas expresivos
- Agrego requerimientos faltantes
- Eliminacion de la clase Cliente
- Agrego clase RegistroVentas

## Aclaraciones

- La relacion Venta CONOCE Prenda se describe como Venta(1) posee Prenda(1...*)
- La relacion Venta CONOCE FormaDePago se describe como Venta(1) realiza FormaDePago(1)
- La relacion Prenda CONOCE EstadoPrenda se describe como Prenda(1) esta EstadoPrenda(1)
- La relacion RegistroVentas CONOCE Venta se describe como RegistroVentas(1) registra Venta(1...*)