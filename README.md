# Tripwise
Planificación de itinerarios familiares para una agencia de viajes

## Procedencia del problema

La idea nació al intentar organizar unas vacaciones familiares. Elegir qué visitar parecía sencillo hasta que hubo que encajar horarios, duración de las visitas, desplazamientos y presupuesto. En una agencia que prepara viajes a medida, este trabajo se repite para cada cliente y, además, la propuesta suele cambiar mientras se prepara.

Para plantear el proyecto me sitúo en una agencia de viajes local que trabaja con familias. El caso de la agencia sirve para definir quién utilizaría la aplicación; no presupone que haya entrevistado a una empresa concreta ni que conozca su sistema informático actual.

## Descripción del problema

Una familia pide una propuesta para varios días e indica las fechas, las edades de los viajeros, lo que le interesa visitar y cuánto puede gastar. El agente selecciona actividades y las distribuye por jornadas. Después, la familia puede pedir un cambio: sustituir una visita, dejar una tarde libre o reducir el coste.

Cada cambio obliga a revisar el resto de la propuesta. Una actividad puede coincidir con otra, quedar demasiado lejos para llegar a tiempo, no admitir a un menor o hacer que se sobrepase el presupuesto. También puede que el agente haya utilizado una duración o un precio que se haya modificado posteriormente en el catálogo de la agencia. Si estas comprobaciones se hacen una a una, preparar una nueva versión lleva tiempo y es fácil pasar por alto alguna incompatibilidad.

El problema que quiero resolver es, por tanto, cómo preparar y modificar una propuesta de viaje familiar manteniendo visibles sus restricciones de tiempo, adecuación y coste. No se trata de decidir por la familia cuál es el mejor viaje, sino de ayudar al agente a comprobar que la propuesta que le presenta tiene sentido con los datos que conoce.

## Objetivo

Desarrollar una aplicación compartida por los agentes de la agencia. Cada solicitud recogerá los datos de la familia y podrá dar lugar a una o varias versiones del itinerario. Al añadir o mover una actividad, la aplicación calculará el coste estimado y señalará los conflictos de horario, los desplazamientos que no caben entre dos visitas y las restricciones de edad que se incumplan.

Por ejemplo, si una visita termina a las 13:00 y la siguiente comienza a las 13:15, pero el desplazamiento registrado entre ambas zonas requiere 30 minutos, el agente recibirá un aviso antes de enviar la propuesta. Si cambia una actividad de pago, verá también cómo queda el presupuesto familiar.

El agente podrá ajustar el itinerario y decidir qué versión entregar. Mantener las solicitudes, el catálogo y las propuestas en una misma aplicación permitirá que otro agente continúe el trabajo cuando sea necesario.

## Fuente de datos

He consultado la [sección de turismo de datos.gob.es](https://datos.gob.es/es/sectores/turismo) y he elegido como posible punto de partida el conjunto [«Puntos de interés turístico de la ciudad de Madrid. Qué visitar en Madrid»](https://datos.gob.es/es/catalogo/l01280796-puntos-de-interes-turistico-de-la-ciudad-de-madrid-que-visitar-en-madrid-www-esmadrid-com1), publicado por el Ayuntamiento de Madrid. Incluye museos, monumentos y otros lugares visitables, con datos como la dirección, la ubicación y una descripción. En algunos casos aparecen también horarios y costes de acceso. El [archivo en español](https://www.esmadrid.com/opendata/turismo_v1_es.xml) se ofrece en formato XML.


Las [condiciones de reutilización de Madrid Destino](https://datos.madrid.es/pages/condiciones-reutilizacion-informacion-madrid-destino) permiten utilizar los datos y textos para fines comerciales y no comerciales, pero establecen límites diferentes para las fotografías. Por eso, el catálogo inicial utilizará la información textual y de ubicación, sin importar imágenes. Los horarios o costes que aparezcan en la fuente deberán revisarse antes de preparar una propuesta; la disponibilidad de plazas, la duración estimada de cada visita y el precio que aplique la agencia se introducirán por separado.

## Imágenes relacionadas con las fichas del problema y la configuración de git
![Ficha de cliente](/media/cliente.jpg)
![Configuración del repositorio](/config/configuracion.md)