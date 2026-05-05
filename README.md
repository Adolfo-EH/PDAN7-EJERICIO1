# PDAN7-EJERICIO1

📊 CASO PROPUESTO: "Sistema de Gestión Integral y Control de Fidelización para Gimnasio" 🏋️‍♂️
🏦 Contexto del negocio
El gimnasio "Turkys Gym" es un centro de entrenamiento físico que ofrece diversos servicios de salud y bienestar. Actualmente, el gimnasio maneja su información de forma fragmentada, lo que dificulta el seguimiento de los socios, el control de los vencimientos de membresías y la gestión de inventario de la tienda interna (suplementos y bebidas).

La administración ha detectado que muchos socios ingresan con membresías vencidas debido a la falta de un sistema de validación en tiempo real. Además, no se cuenta con un registro histórico de la evolución física de los clientes ni de sus preferencias de compra, lo que impide realizar campañas de marketing dirigidas.

Por ello, se busca desarrollar una base de datos robusta que permita:

Controlar el acceso y la vigencia de las membresías de forma automatizada.

Gestionar el inventario y las ventas de la tienda de suplementos.

Monitorear el rendimiento financiero y la asistencia de los socios.

Generar alertas de renovación para evitar la fuga de clientes.

🎯 Objetivo del sistema
Diseñar una base de datos que permita:

Registrar la información detallada de socios y personal (entrenadores/administrativos).

Gestionar diversos planes de entrenamiento y membresías.

Controlar el flujo de caja mediante el registro de pagos y ventas de productos.

Administrar el control de acceso mediante registros de asistencia.

Evaluar el progreso físico de los socios mediante métricas corporales.

🧩 Alcance funcional
1. 👤 Gestión de Socios y Staff
El sistema debe diferenciar entre:

Socios: DNI, nombres, apellidos, fecha de nacimiento, contacto, y estado de salud inicial.

Staff: Datos personales, cargo (entrenador, recepcionista), horario de turno y sueldo.

2. 💳 Membresías y Planes
El gimnasio ofrece planes flexibles:

Tipos: Diario, Mensual, Trimestral, Anual.

Categorías: Solo máquinas, Full (incluye clases grupales), VIP (incluye personal trainer).

Cada plan tiene un precio base y una duración en días.

3. 📝 Contratos y Renovaciones
Cuando un socio adquiere un plan:

Se registra la fecha de inicio y se calcula automáticamente la fecha de fin.

Estado del contrato: Activo, Congelado (por salud), Vencido.

Un socio puede haber tenido muchos contratos a lo largo del tiempo (historial).

4. 🏪 Gestión de Ventas (Tienda)
El gimnasio vende productos adicionales:

Productos: Nombre, categoría (proteínas, hidratantes, ropa), stock mínimo, stock actual y precio de venta.

Ventas: Registro de qué producto se vendió, cantidad, fecha y quién realizó la venta.

5. 🕒 Control de Asistencia y Acceso
Cada vez que un socio llega:

Se registra la fecha y hora de entrada.

El sistema debe validar si el socio tiene un contrato Activo. Si está vencido, se genera una alerta.

6. 📈 Seguimiento Antropométrico
Para dar valor agregado, los entrenadores registran:

Fecha de evaluación.

Peso, % de grasa, masa muscular, medidas de pecho, brazo, cintura, etc.

Esto permite ver la evolución del socio en el tiempo.

📈 Reglas de negocio clave
Un socio solo puede tener un contrato Activo a la vez.

La asistencia solo se registra si el contrato vigente está pagado y no vencido.

El stock de productos debe disminuir automáticamente con cada venta.

Un entrenador puede estar asignado a varios socios, pero un socio solo tiene un entrenador de cabecera en sus planes VIP.

Los precios de las membresías pueden variar, pero se debe respetar el precio pactado en el contrato firmado.
