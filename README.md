# Proyecto_1_Billeteraelectronica




## Caso: Billeteras Electrónicas

Las billeteras electrónicas no solo han transformado la forma en que pagamos, sino que también han sido clave para mejorar la seguridad, la accesibilidad y la eficiencia de las transacciones financieras. Son una herramienta esencial para la sociedad moderna, promoviendo el uso de pagos digitales y ofreciendo nuevas oportunidades para la gestión financiera tanto a nivel personal como empresarial.

ESQUEMA: Entidad | Relación

1. Identificación de entidades principales:

Usuario: Para manejar a los usuarios del sistema.
Método de pago: Tarjetas de crédito/débito   asociadas.
Transacción: Registra todas las operaciones financieras.
Comercio: Información sobre los comercios afiliados.


2. Atributos de cada entidad:

Usuario:

- IDUsuario (PK)
- Nombre
- Correo
- Teléfono
- Contraseña
- BalanceActual


Método de pago:

- IDMetodoPago (PK)
- Tipo (Tarjeta, Cuenta bancaria)
- Número
- Banco
- FechaExpiración (si aplica)
- IDUsuario (FK)


Transacción:

- IDTransaccion (PK)
- Monto
- FechaHora
- TipoTransaccion (Depósito, Retiro, Pago)
- IDUsuarioOrigen (FK)
- IDUsuarioDestino (FK, nullable para retiros y depósitos)
- IDComercio (FK, nullable para transacciones entre usuarios)


Comercio:

- IDComercio (PK)
- Nombre
- TipoNegocio
- Ubicación


## Modelo Entidad | Relación
