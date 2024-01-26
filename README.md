
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

### Uso
```
from influxdb import InfluxDBClient  
lista=[]
lista.append( {
    "measurement" : "metrica_X",
    "tags" :  {"tag_1" : "xx" , "tag_2" : "yy" },
    "time" : var_time_ns,
    "fields" :  {"campo_1" : 55 ,  "campo_2" : 999} 
} )
lista.append( {
    "measurement" : "metrica_Y",
    "tags" :  {"tag_1" : "xx" , "tag_2" : "yy" },
    "time" : var_time_ns,
    "fields" :  {"campo_1" : 55 ,  "campo_2" : 999} 
} )
influxlib.write_points(lista, host='IP_donde_insertaran', username='user_db', password='passwd_db', database='db_nombre', port=8086, debug=1 )
```
