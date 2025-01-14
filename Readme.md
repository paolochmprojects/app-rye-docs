# Manual de Usuario de App Rye

Version 1.0.0 - App Rye

## Tabla de Contenidos

1. Introducción
2. Tipos de Usuarios
3. Primeros Pasos
4. Páginas principales.
5. Páginas restringidas.

## 1. Introducción

Bienvenido al Manual de Usuario de App Rye. Esta guía te ayudará a entender cómo usar la aplicación
de manera efectiva.

## 2. Tipos de Usuarios

App Rye soporta diferentes tipos de usuarios, cada uno con permisos y capacidades únicas. A
continuación se presentan los tipos de usuarios:

### SuperAdmin

Usuario con todos los accesos y vistas de todas las empresas que este subidas a la base de
datos de Rye, como tambien el accesso a las herramientas de administraión internas.

### Owner

Usuario que esta ligado asignado como primer usuario a la compañia registrada en el onboarding,
por el cual puede seguir invitando a más miembros a su compañia y gestionando más operaciones en
la compañia.

### Admin

Usuario que puede hacer lo mismo que Owner, la diferencia es que no puede retirar los atributos
del usuario Owner, ni Superadmin.

### Guest

Usuario que sólo puede ver ciertas vistas y es getionado por los usarios SuperAdmin, Owner
y Admin.

## 3. Primeros Pasos

Al completar el incio de sesión se redirigirá a la primera vista (Home) con la data de
empresa que este asociada a los usuarios Owner, Admin y Guest, en el caso de SuperAdmin será
con la información de la empresa que haya seleccionado.

### Barra de navegación y pié de página

Entre las vistas se podrá visualizar la barra de navegación y el pié de página:

- Barra de navegación: Se mostrará el logo de Rye, las páginas que se puede navegar y el
  botón de account settings, en el caso de los SuperAdmin se hará visible el seleccionador
  de compañías.

- Pie de página: Mostrará el un bóton para solicitar asistencia al equipo de Rye.

### Account Settings

Este es el aparto para gestionar algunas características de la cuenta actual, en los siguientes
apartados:

- Account: Aqui se mostrará un form para poder cambiar el correo de la cuenta actual, al
  solicitarlo enviará un email a correo actual un link, al hacer click el pricedimiento será
  automático.

- Team: Aquí podrás encontrar el asistente, para controlar el acceso de nuevos miembros a la
  compania actualmente se encunetra seleccionado.

- Billing: Esto esta en construccion.

- Admin Tools: Esto sólo será visible para los usuarios SuperAdmin, aquí se podrá ver un
  bóton para poder ingresar a las herramientas de admintrador.

## 4. Páginas principales

### Home

Esta vista esta compuesta por varios componentes, que muestra data relevante de estado de las
cuentas de la compañia seleccionada.

- Portafolio balance: Muestra el balance de la compañia, acompañado de un bóton de asistencia
  con el equipo de rye.

- Spend and Savings: Muestra la grafica de los gastos y ahorros de la compañia, por defecto
  mostrar los datos del año actual, los datos pueden ser ajustados con los filtros para
  ajustar su visualización, por todos los sitios o sitios seleccionados, por el año, por
  mes o trimestre, además de tener 2 indicadores en la parte superior que muestra el
  totalizado tanto de gastos y ahorros.

- Portafolio: Muestra una tabla con la información de las facturas de cada mes, monstrando el
  estado en la que se encuentra y con la posibilidad de poder ser descargas o enviadas al correo
  del usuario actual, además si el sitio presenta más de un MPAN asociado, estos se verán
  reflejados en la tabla, además de contar con los filtros por el tipo y status de las
  facturas.

#### Formulario Add Site

Este formulario sólo se mostrará para los usuarios Owner, Admin y SuperAdmin, para poder agregar
un nuevo sitio a la compañia actual. Este formulario cuenta con 2 tipos de modos:

- Modo automático: En el modo automático se requiere de una factura anterior, de la
  cual se extraerá la data que se requiere para la creacion de un sitio.

- Modo manual: Los datos requeridos se deberán ingresar de forma manual en base el
  formulario lo vaya solicitando.

Enambos casos si el sitio a añadir tiene más de un MPAN asociado, en el input correspondiente
debera ser agregado y separado con comas.

### Intelligence

Esta vista esta compuesta por varios componentes, que muestra data relevante de estado de las
cuentas de la compañia seleccionada. Enfocadas al bussines intelligence.

- Site by site comparison: Este componente muestra todos los sitios de forma agrupada filtrado
  por dos parametros los sitios a visualizar y el año, se podrán cambiar entre datos de interés:

  - Total Spend.
  - Total Savings.
  - Total Energy Usage.

- Food Safety: Herramienta en construcción.

- Energy Usage: Este componente muestra un gráfico lineal de los consumos que se han registrado
  en los sitios seleccionados, en meses o trimestres y en el año.

- Total Savings: Este componente muestra un gráfico de barras de los ahorros totales que se han
  logrado en los sitios seleccionados, en meses o trimestres y en el año.

- Forecast: Herramienta que sirve para ver la proyección de consumos de electricidad que y gastos
  que se tendría al abrir un nuevo sitio, en base a los dias y horas de operacion del nuevo sito
  proyectado.

- Smart cooling: Muestra un formulario de opciones múltiples, para escoger que tipo de herramientas
  se desea ver en proximas actualizaciones. Opciones a escoger.
  - Food Safety Monitoring.
  - Electrical System Design for New Sites.
  - Savings on Smart Refrigeration.

### Documents

Esta vista esta orientada a la gestión documentaría, para cada sitio registrado en cada compañía,
se mostrará una grilla para los siguientes documentos:

- Schematic
- Landlord Contract
- Supplier Contract

El usuario Owner solo podra, ver los documentos y no actualizarlos.

## 5. Páginas restringidas.

Estas vistas estan limitadas sólo para los usuarios SuperAdmin.

### Barra de navegación

Entre las vistas se podrá visualizar la barra de navegación:

- Barra de navegación: Se mostrará el logo de Rye, las páginas que se puede navegar y el
  botón de "Go to dashboard", que te permitirá regresar a las vista anterior.

### Onboarding

Esta vista mostrará las distintas herramientas para administradores, para el registro de
distintos tipos datos usuarios empresas o ambos, con distintos flujos.

#### New users

Se mostrará una tabla para añadir nuevos usuarios mediante filas, de los cuales son requeridos
su correo electrónico y un role asignado como los detallos en el principio, la asignación de
la compañia es opcional. Debajo de la tabla existe un botón para ir añadiendo mas filas. Una vez
completado se podrá dar al botón confirmar para guardar los cambios.

#### New companies

Se mostrará una tabla para añadir nuevas compañias mediante filas, de los cuales sólo se necesita
el nombre de la nueva compañia, y la asignación usuarios y sitios es opcional pero recomendada.
Debajo de la tabla existe un botón para ir añadiendo mas filas. Una vez completado se podrá dar
al botón confirmar para guardar los cambios.

#### New sites

Formulario de multiples pasos, para la creacion de nuevos sitios.

- Pasos:

  - Upload: En este paso se deberá cargar facturas antiguas para iniciar con
    formulario.

  - Sites Details: En este paso se deberá asignar a que compañia pertenece el
    nuevo sitio que se creará, y tambuen los datos de localización del sito.

  - Energy Supply information: En este paso llena los datos correpondientes al
    energy supply, meter (live o estimate) que sera un switch, el nombre de supplier
    y el MPAN asociado a este.

  - Historical Tariff Data: En este paso se deberá añadir, las tarifas correspondientes
    de las facturas que se cargarons en un inicio.

  - Confirm: En este paso se podrá previsualizar el los datos que serán guardados, antes
    de dar al botón de confirmar.

#### Add documents

Se mostrará una tabla para añadir documentos a los sitios registrados, se podrán aplicar filtros
por compañia y sitios, además de poder subir los documentos en formato PDF de forma independiente
a través de un modal.

#### Complete Onboarding

Formulario de multiples pasos, para la creacion de empresas, sitios, gestion de documentaría
y usuarios de una empresa.

- Pasos:

  - Add Companies: En este paso se podrá visualizar una tabla en la que se podrá añadir los nombre de
    las compañias que se van a crear. En la parte inferior existe un botón para añadir más filas
    según se requiera.

  - Add Users: En este paso se podrá visualizar una tabla, en la cual debera asignar una de las compañias
    que se esta creando, el rol de usuario y el email con el que iniciar sesión.

  - Add Sites: En este paso se encuentra divido en dos subpasos, primero se mostrara un asistente para poder subir archivos, una ves confirmado, cambiará al segundo subpaso que mostrara una tabla que habrá en donde se habrá generado tantas filas como facturas se hayan subido, se deberá asignar a que compañia pertenece cada sitio por crear, y rellenar el resto de dato.

  - Add Documentes: En este paso se visualizará una tabla, con los sitios que se añadiran y campos en los cuales se deberá subir
    los documentos respectivos en formato PDF, de existir un archivo equivacado se podrá reemplazar en el mismo campo.

  - Confirm: En este paso se deberá previsualizar los datos y archivos que crearan agrupados en su respectiva compañia antes de ser subidos al sistema y dar al botón confirmar para terminar con el formulario.

### Monthly readings

Esta vista muestra diferentes herramientas relacionadas a las facturas mensuales
de los sitios.

#### Uploads readings x

Formulario de mutiples pasos para el carga de nuevas facturas facturas y datos.

- Pasos:

  - Upload: En este paso se podrán cargar las facturas que seran procesadas para la extracción
    de datos, este puede tradar algunos segundos dependiendo de la cantidad de archivos a subir,
    si se visualiza la advertencia de que no se puedo procesar alguno de los documentos, podrá
    seguir con los siguientes pasos de forma manual.

  - Assign sites: En este paso se podrá asignar a que sitio y compañia pertenece la factura que
    se va a cargar. Se incluye una botón para visualizar la factura correspondiente a subir.

  - Billing information: En este paso será rellenada con la información obtenida en la extracción
    de datos del paso "Upload", en caso de fallar, los campos se pueden rellenar de forma manual.

  - Energy Usage Details: En este paso será rellenada con la información obtenida en la extracción
    de datos del paso "Upload", en caso de fallar, los campos se pueden rellenar de forma manual.

  - Next Steps: En este paso se podrá rellenar ciertas caracteristicas, de las facturas a subir como
    de que tipo son, la action recomendada y si esta ya esta pagada.

  - Confirm: En este paso de podrá visualizar los datos antes de ser subidos al sistema y dar al botón para terminar con el formulario.

#### Deleted incorrect readings

Formulario de mutiples pasos para el borrado de facturas en el sistema.

- Pasos:

  - Filter: En este paso se podrán hacer filtrado por company, sites, month,
    supplier, invoice type and status de las facturas.

  - Select: En este paso podrás selecionar las facturas a borrar, en el
    siguiente paso.

  - Confirm: En este paso se previsualizarán las facturas que serán eliminadas
    del sitema antes de dar al botón de confirmar para terminar el formulario.

#### Update readings

Formulario para la actualización de facturas y datos de lecturas en el sistema.

- Pasos:

  - Filter: En este paso se podrán hacer filtrado por company, sites, month,
    supplier, invoice type and status de las facturas.

  - Select: En este paso podrás selecionar las facturas a actualizar, en el
    siguiente paso.

  - Edit: En este paso se podrán editar las facturas que han sido seleccionado
    en el paso anterior.

  - Confirm: En este paso se previsualizarán los datos que se actualizar antes
    de dar al botón de confirmar para terminar el formulario.

### Update

Esta vista muestra un formulario multi-step para la actualización de la datos
relacionados al MPAN, tarifas antiguas y nuevas.

El formulario cuenta con una visualización del paso actual y los siguientes.

- Pasos:

  - Filter: Se puede filtrar entre companies y sitios para obtener los MPAN.

  - Edit: Se puede editar los MPAN que han sido filtrado en el paso anterior.

  - Confirm: Se puede mostrar los datos antes de actualizar antes dar al botón
    de confirmar para terminar el formulario.
