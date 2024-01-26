
# jipamlib_influxdb_v1  
librería para insertar a influxdb v1  

## install  
```
pip3 install jipamlib_influxdb_v1  
```
## parámetros

- list: (requerida, string) lista de métricas en formato json  
- host: (requerida, string) ip o hostname de influxdb  
- username: (requerida, string) nombre de usuario  
- password: (requerida, string) contraseña  
- database: (requerida, string)  database a insertar
- port: (opcional, int, default=8086) puerto destino
- attempts: (opcional, int, default=10) reintentos máximos en caso de falla  
- sleep_on_fail: (opcional, int , default=2) segundos a esperar antes de reintentar una inserción fallida
- batch_size: (opcional, int, default=500) número de métricas a insertar por lote  
- debug: (opcional, int, default=1)  1 para modo verboso, 0 para imprimir solo errores  


