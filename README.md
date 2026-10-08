# Examen_mysql_2
1. Vista de Estado de Espacios (VW_EstadoEspacios)
Lo que hiciste: Creaste una vista que lista todos los espacios de trabajo disponibles en el sistema.

Qué hace: Muestra el nombre, tipo y estado actual de cada espacio, agregando un campo calculado que busca cuál es su próxima reserva programada. Para ello, filtra únicamente las reservas en estado Confirmada o Pendiente desde la fecha actual en adelante (CURDATE()), ordenándolas por fecha y hora para mostrar la más cercana.

2. Procedimiento Almacenado de Reporte Diario (sp_GenerarReporteDiario)
Lo que hiciste: Creaste un procedimiento almacenado que recibe como parámetro una fecha específica (p_fecha).

Qué hace: Consolida y devuelve un resumen financiero y operativo del día solicitado con tres indicadores clave:

Total de Reservas: Cuenta cuántas reservas válidas se registraron en el día (excluyendo las canceladas).

Usuarios Activos: Cuenta la cantidad de personas únicas que ingresaron y fueron autorizadas en las instalaciones.

Ingresos del Día: Suma el total del dinero recibido por pagos en estado Pagado. Si no hubo ingresos en esa fecha, devuelve 0.00 automáticamente.

3. Consulta de Aforo en Tiempo Real
Lo que hiciste: Escribiste una consulta de conteo filtrando por una fecha específica (en este caso '2026-09-30').

Qué hace: Revisa los registros de asistencia para determinar cuántas personas permanecen actualmente dentro del coworking. Filtra únicamente a los usuarios que fueron autorizados a ingresar en esa fecha y cuya hora de salida no se ha registrado aún (hora_salida IS NULL), formateando el resultado en un mensaje de texto claro sobre el estado del aforo.

1 prueba de la vista VW_EstadoEspacio
<img width="1341" height="615" alt="image" src="https://github.com/user-attachments/assets/5d4f3d4a-5268-4c14-aebf-69026d4a4342" />
2 prueba del procedimiento
<img width="1358" height="575" alt="image" src="https://github.com/user-attachments/assets/98aa30b4-9e45-4880-8120-b79581f456fd" />
3 prueba de la consulta
<img width="1383" height="342" alt="image" src="https://github.com/user-attachments/assets/259ae9ac-3270-411b-acb9-7f7228e1c5f3" />

