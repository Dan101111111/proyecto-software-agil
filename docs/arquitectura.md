# Arquitectura tecnológica

## 1. Descripción general

El proyecto de comercio electrónico propone una arquitectura tecnológica basada en componentes desacoplados. Este modelo arquitectónico separa claramente la capa de presentación (interfaz de usuario), la capa de lógica de negocio y servicios (API), y la capa de persistencia (almacenamiento de datos). Esta separación de responsabilidades asegura un código más limpio, facilita el mantenimiento a largo plazo y permite la escalabilidad independiente de las diferentes partes del sistema.

## 2. Componentes

### Frontend — Next.js
Representa la capa de presentación de la plataforma. La función principal de Next.js será proporcionar la interfaz visual interactiva con la cual el cliente (a través de su navegador) navega por el catálogo, gestiona su carrito de compras y realiza el proceso de pago. 

### Backend — FastAPI
Actúa como el núcleo o motor lógico de la aplicación. La función de FastAPI es exponer una Interfaz de Programación de Aplicaciones (API) que se encarga de recibir, validar y procesar las solicitudes generadas por el frontend. Aquí residirán las reglas de negocio, la validación de seguridad y la orquestación para conectar las solicitudes de los usuarios con la base de datos.

### Base de datos — PostgreSQL
Funciona como el sistema gestor de bases de datos relacional. La función de PostgreSQL es almacenar, consultar y gestionar de forma persistente e íntegra toda la información crítica del ecosistema, incluyendo el catálogo de productos, cuentas de clientes, historiales de pedidos y registros de pagos.

## 3. Flujo de comunicación

El flujo principal de datos y solicitudes del sistema se estructura mediante el siguiente ciclo cliente-servidor:

**Cliente → Next.js → FastAPI → PostgreSQL**

1. **Cliente:** Un usuario ingresa al e-commerce desde su dispositivo e interactúa con un elemento de la pantalla (ej. hacer clic en un producto).
2. **Next.js (Frontend):** Capta la interacción y, en caso de necesitar información dinámica, envía una solicitud HTTP (usualmente mediante JSON) hacia el servidor de backend.
3. **FastAPI (Backend):** Recibe la petición, verifica credenciales o permisos, procesa la lógica necesaria para cumplir el requerimiento y lo traduce en una consulta formal para la base de datos.
4. **PostgreSQL (Base de datos):** Ejecuta la consulta SQL solicitada y retorna la información persistida (ej. disponibilidad en stock y precio).
5. **Retorno:** FastAPI procesa los datos obtenidos, los empaqueta como respuesta a Next.js, y finalmente, el frontend renderiza la información en la pantalla del usuario.

## 4. Estructura del proyecto

Para soportar esta arquitectura de forma organizada y modular, el repositorio se estructura físicamente en los siguientes subdirectorios principales:

*   **`frontend/`**: Su finalidad es contener estrictamente los códigos fuente de Next.js (rutas, componentes visuales de React, estilos CSS y gestión del estado en el cliente).
*   **`backend/`**: Su finalidad es aislar el código fuente de FastAPI (controladores, definiciones de rutas de la API, modelos de negocio, esquemas de validación y la configuración de conexión a la base de datos).
*   **`docs/`**: Su finalidad es agrupar toda la documentación académica y técnica del proyecto, incluyendo manuales, investigaciones metodológicas (como el Manifiesto Ágil y el cuadro comparativo) y especificaciones arquitectónicas.

## 5. ¿Por qué esta arquitectura se beneficia de un enfoque ágil?

La elección de una arquitectura desacoplada (Frontend / Backend / Base de Datos) es ideal para implementarse mediante metodologías ágiles por las siguientes razones:

*   **Desarrollo incremental:** Al no ser un bloque monolítico rígido, el equipo puede construir pequeñas partes operativas de cada componente. Por ejemplo, programar solo un controlador básico en FastAPI y su contraparte en Next.js, sin requerir diseñar el sistema completo por adelantado.
*   **Desarrollo de funcionalidades por iteraciones:** Permite a los equipos trabajar en historias de usuario completas que atraviesan todas las capas. En un solo "sprint" o iteración, el equipo entrega la funcionalidad de "Ver carrito de compras" funcionando desde Next.js hasta PostgreSQL.
*   **Entregas progresivas:** La separación facilita empaquetar y liberar pequeñas versiones funcionales tempranas al mercado, aportando valor al cliente y cumpliendo el principio ágil de realizar entregas tempranas y continuas de software funcionando.
*   **Incorporación ágil de cambios:** Un sistema modular abraza el cambio. Si se necesita renovar por completo el diseño visual de la tienda, solo se afecta el código de Next.js; si las reglas de cálculo fiscal varían, solo se edita FastAPI. Esto minimiza el riesgo de quebrar toda la plataforma al introducir nuevos requerimientos.
*   **Colaboración y autoorganización del equipo:** Los desarrolladores pueden dividirse en roles especializados (frontend y backend) que trabajan en paralelo sin bloquearse mutuamente. Esto fomenta equipos autónomos que se comunican continuamente estableciendo "contratos" de API para interactuar de forma ordenada.
