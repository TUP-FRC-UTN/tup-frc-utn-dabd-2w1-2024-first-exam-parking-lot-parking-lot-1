# Sistema de Gestión de Playa de Estacionamiento
El sistema a desarrollar es para una playa de estacionamiento que permite el ingreso y estadía de motocicletas, automóviles y camionetas. 
La playa de estacionamiento posee 30 plazas (slot), y la asignación de estas plazas se explica más adelante.
El objetivo de este desarrollo es poder registrar el ingreso de cada vehículo, mostrando la disponibilidad de espacios libres y ocupados con sus respectivos vehículos, asignando de forma automática el vehículo que ingresa a un lugar disponible y válido. 

## Requisitos Funcionales

1. **Mostrar Distribución de Lugares y Disponibilidad:**
   - **Distribución:** Mostrar el diseño del estacionamiento con la disponibilidad de los lugares. Utiliza diferentes íconos para representar los distintos tipos de vehículos:
     - **Lugar Disponible:** Mostrar un punto para los lugares disponibles.
     - **Lugares Ocupados:** Utiliza íconos de Bootstrap para mostrar autos, camionetas o motocicletas en los lugares ocupados.
   
2. **Formulario de Ingreso de Vehículo:**
   - **Campos del Formulario:**
     - **Marca** (Requerido): Proporcionar una lista predefinida de marcas.
     - **Modelo** (Opcional): Mínimo de 3 caracteres.
     - **Dominio Nuevo** (Booleano): Indica si el vehículo tiene un dominio nuevo.
     - **Dominio** (Requerido, X Caracteres Exactos): siendo X 7 para dominios nuevos y 6 para dominios viejos.
     - **Tipo de Vehículo**: Seleccionar de un enumerado con valores: moto, auto, camioneta.
     - **Hora de Ingreso** (Requerido): Debe ser proporcionada. Cargar la hora actual por defecto.
   - **Validación:**
     - Mostrar errores solo después de que el usuario haya interactuado con los controles del formulario.
   
3. **Visualización de Una Pantalla a la Vez:**
   - **Visibilidad del Formulario y del Mapa:**
     - Mostrar solo el formulario o el mapa, pero no ambos simultáneamente.
     - El formulario debe estar oculto mientras se visualiza el mapa y viceversa.
     - El usuario debe poder navegar entre ver el formulario y el mapa por medio de botones.
   
4. **Asignación de Lugares de Estacionamiento:**
   - **Tipo de Vehículo y Asignación de Lugares:**
     - Asignar los lugares de estacionamiento según el tipo de vehículo (cada plaza tiene 8 lugares y puede recibir varios vehiculos mientras haya espacio disponible):
       - **Camioneta:** Requiere 8 lugares.
       - **Auto:** Requiere 4 lugares.
       - **Motocicleta:** Requiere 1 lugar.
   Es decir, en una plaza entra solo una camioneta o, dos autos u, ocho motos. Entonces, si en una plaza hay un auto solamente, pueden entrar en la misma plaza hasta cuatro motocicletas.  
   - **Actualización de Disponibilidad:**
     - Al ingresar un vehículo, buscar un lugar disponible según el tipo de vehículo y actualizar la visualización del estacionamiento en consecuencia.
   
5. **Visualización de los Lugares:**
   - **Lugares Ocupados y Disponibles:**
     - **Ocupados:** Mostrar los lugares en rojo.
     - **Disponibles:** Mostrar los lugares en verde.
   - **Claridad:** Proporcionar indicadores visuales claros para ayudar al encargado de la playa de estacionamiento a identificar fácilmente los lugares ocupados y disponibles.

## Consideraciones

- **Estructura de Archivos:** Organizar los archivos en directorios según sus responsabilidades.
- **Estilo:** Respetar los estilos proporcionados utilizando el framework (Bootstrap).
- **Idioma:** Escribir todo el código y los comentarios en inglés, pero los mensajes dirigidos al usuario (etiquetas, alertas, validaciones, etc.) deben estar en español.
- **Archivos Proporcionados:** No modificar ningún archivo proporcionado, excepto el del formulario.
- **SPA** La pagina nunca debe ser recargada ateniendose al mecanismo proporcionado por las aplicaciones de una sola página.

## MockUps
![image](https://github.com/user-attachments/assets/3279d9de-f4ea-45fc-895d-95f3f488a7f8)
![image](https://github.com/user-attachments/assets/2a1acc62-9738-40cc-9e8f-54449902ac9e)
![image](https://github.com/user-attachments/assets/84358f1f-287d-4d79-b0dc-516d35a92ff1)


## Ejemplos: 
Teniendo en cuenta la primer imagen proporcionada como mock up de la disponibilidad de lugares, a continuación se presentan algunos ejemplos visuales indicando como debería quedar la disponibilidad de lugares al ingresar un nuevo vehiculo:

**En caso de agregar una moto:**
![image](https://github.com/user-attachments/assets/99b6558d-7f39-48fb-a381-a19ee1c4f4ba)

**En caso de agregar un auto:**
![image](https://github.com/user-attachments/assets/9171d8a9-099f-4c7e-a747-dda5452357b2)

**En caso de agregar una camioneta:**
![image](https://github.com/user-attachments/assets/722bef2b-74b3-40c2-a5bd-3f63f299677a)

## Rubrica:
- Registro ingreso (3)
- Validaciones (2)
- Mapa playa estacionamiento (3)
- Navegación componentes (1)
- Estilos (1)