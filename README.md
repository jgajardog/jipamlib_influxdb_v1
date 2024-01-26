# jipamlib_influxdb_v1  
libreria para insertar a influxdb v1  

## install  
```
pip3 install jipamlib_influxdb_v1  
```
## parametros

- list: (mandatoria) lista de metricas en formato json  
- host: (mandatoria) ip o hostname de influxdb  
- username: (mandatoria) nombre de usuario  
- password: (mandatoria) contraseña  
- database: (mandatoria)  database a insertar
- port: (opcional, default=8086) puerto destino
- attempts: (opcional, default=10) reintentos maximos en caso de falla  
- sleep_on_fail: (opcional, default=2) segundos a esperar antes de reintentar una insercion fallida
- batch_size: (opcional, default=500) numero de metricas a insertar por lote  
- debug: (opcional, default=1)  1 para modo verboso, 0 para imprimir solo errores
