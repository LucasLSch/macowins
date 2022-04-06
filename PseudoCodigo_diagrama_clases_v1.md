class Prenda{
	const tipoPrenda
	var precioBase

	method obtenerTipoPrenda(){
		return tipoPrenda
	}

	method calcularPrecioPrenda()
}

class PrendaNueva inherits Prenda{
	method calcularPrecioPrenda(){
		return self.precioBase()
	}
}

class PrendaPromocion inherits Prenda{
	var valorDto

	method calcularPrecioPrenda(){
		return precioBase - valorDto
	}
}

class PrendaLiquidacion inherits Prenda {
	method calcularPrecioPrenda(){
		return precioBase * 0.5
	}
}

class Cliente{
	const nroCliente
	var prendasEnCarrito = new List()
	
	/* Metodos para agregar sacar prendas */
	/* Para aclarar que Cliente conoce Prenda */
	method agregarACarrito(prenda){
		prendasEnCarrito.add(prenda)
	}
	method eliminarDelCarrito(prenda){
		prendasEnCarrito.delete(prenda)
	}

	method comprar(tipoPago){
		var venta = new Venta(prendasVendidas = prendasEnCarrito,
				  cantidad = prendasEnCarrito.length(),
				  fechaVenta = new Date(),
				  formaDePago = tipoPago)
		self.pagar(venta.totalAPagar(), tipoPago)
	}

	method pagar(monto, tipoPago){...}

	method consultarTipoPrenda(prenda){
		var tipoPrenda = prenda.obtenerTipoPrenda()
		...
	}
	
	method consultarPrecio(prenda){
		var precioPrenda = prenda.calcularPrecioPrenda()
	}
}

class Venta{
	const prendasVendidas
	const cantidad
	const fechaVenta
	const formaDePago

	method totalAPagar(){
		var montoAPagar = prendasVendias.map({prenda => formaDePago.obtenerPrecioFinal(prenda.obtenerPrecioPrenda())}).sum()
		...
		return montoAPagar
	}
}

class Efectivo{
	method obtenerPrecioFinal(precioPrenda){
		return precioPrenda
	}
}

class Tarjeta{
	const cantidadCuotas

	method obtenerPrecioFinal(precioPrenda){
		return precioPrenda + cantidadCuotas * COEFICIENTE_RECARGO + 0.01 * precioPrenda
	}
}