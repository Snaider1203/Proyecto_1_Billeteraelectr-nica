# Proyecto_1_Billeteraelectronica


ESQUEMA: Entidad | Relación

Caso: Billeteras Electrónicas

1. Identificación de entidades principales:

Usuario: Para manejar a los usuarios del sistema.
Método de pago: Tarjetas de crédito/débito   asociadas.
Transacción: Registra todas las operaciones financieras.
Comercio: Información sobre los comercios afiliados.


2. Atributos de cada entidad:

Usuario:

IDUsuario (PK)
Nombre

Correo

Teléfono

Contraseña

BalanceActual


Método de pago:

IDMetodoPago (PK)
Tipo (Tarjeta, Cuenta bancaria)
Número
Banco
FechaExpiración (si aplica)
IDUsuario (FK)


Transacción:

IDTransaccion (PK)
Monto
FechaHora
TipoTransaccion (Depósito, Retiro, Pago)
IDUsuarioOrigen (FK)
IDUsuarioDestino (FK, nullable para retiros y depósitos)
IDComercio (FK, nullable para transacciones entre usuarios)


Comercio:

IDComercio (PK)
Nombre
TipoNegocio
Ubicación



