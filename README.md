📊 CASO PROPUESTO: "Sistema de Gestión Transaccional y Control de Membresías - Turkys Gym" 🏋️‍♂️

🏦 Contexto del negocio
El gimnasio Turkys Gym es una empresa dedicada al rubro del bienestar físico que ofrece servicios de entrenamiento y venta de productos nutricionales. Actualmente, el negocio maneja su información de manera aislada: las ventas de productos no están vinculadas correctamente a los comprobantes de pago, y el control de socios no permite un seguimiento histórico claro de quién autorizó cada ingreso o venta.

Para mejorar su competitividad y orden administrativo, el gimnasio requiere un sistema de base de datos relacional que integre la gestión de su personal (staff), la fidelización de sus clientes, el control de stock de productos y la facturación detallada de cada transacción.

🎯 Objetivo del sistema
Diseñar una base de datos normalizada que permita:

Centralizar los datos personales de trabajadores y clientes para evitar redundancia.

Gestionar el catálogo de productos por categorías y controlar el inventario.

Registrar la venta de productos y membresías mediante un esquema de cabecera-detalle.

Emitir comprobantes de pago vinculados a cada transacción comercial.

Controlar el acceso diario de socios (asistencia) validando la vigencia de sus membresías.

🧩 Alcance funcional
1. 👤 Gestión de Identidades (Personas)
El sistema debe centralizar los datos básicos en una entidad núcleo:

Persona: Registro de DNI, nombres, apellidos, fecha de nacimiento, sexo, dirección, teléfono y correo.

Cliente: Vinculado a una persona, registra su estado de fidelización.

Trabajador: Vinculado a una persona, incluye su cargo y horario.

2. 🔐 Seguridad y Usuarios
Para la operación del sistema, se debe gestionar:

Usuarios: Solo los trabajadores autorizados tendrán un nickname y clave para acceder al sistema y realizar transacciones.

3. 📦 Catálogo de Productos y Membresías
El gimnasio ofrece tanto bienes físicos como servicios:

Categorías: Clasificación de ítems (Suplementos, Bebidas, Ropa, Planes de Entrenamiento).

Producto: Registro de nombre, precio de venta, stock actual y stock mínimo.

Membresía: Vinculación de un cliente con un tipo de membresía (Mensual, Trimestral, Anual) que define una fecha de inicio y una fecha de fin de acceso.

4. 💰 Proceso de Ventas y Facturación
Cada vez que se realiza una transacción:

Venta (Cabecera): Registra la fecha, el método de pago (Efectivo, Tarjeta, Yape/Plin), el monto total, el cliente que compra y el usuario que realiza la venta.

Detalle de Venta: Desglose de los productos o membresías adquiridas, indicando cantidad, precio unitario y descuentos.

Comprobante: Generación de la serie y el número correlativo (Boleta o Factura) para legalizar la venta.

5. 🕒 Control de Operaciones Diarias

Asistencias: Registro de cada ingreso al gimnasio, capturando la fecha, hora, el cliente que ingresa y el trabajador (usuario) que valida dicho ingreso.

📈 Reglas de negocio clave
Tanto clientes como trabajadores deben estar registrados previamente en la tabla maestra de personas.

Una venta puede contener múltiples productos (detalle), pero genera un único comprobante de pago.

El stock de los productos debe descontarse automáticamente al confirmarse una venta.

El tipo de membresía define la duración en días, la cual se utiliza para calcular la fecha de vencimiento al momento de la compra.

Solo los trabajadores con un registro activo en la tabla de usuarios pueden registrar ventas y asistencias.
