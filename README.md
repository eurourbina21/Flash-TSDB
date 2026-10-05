Flash-TSDB

Motor de Base de Datos de Series Temporales para Flash/SD

Almacenamiento binario de ultra-alto rendimiento construido sobre RT-Serial Kernel


QUE ES FLASH-TSDB

Flash-TSDB es un motor de base de datos de series temporales escrito en C puro, 
diseñado específicamente para dispositivos con almacenamiento Flash/SD (Raspberry Pi, 
gateways industriales, microcontroladores con flash externa).

Optimizado para entornos de recursos limitados, ofrece rendimiento comparable a 
InfluxDB con una huella de memoria 100x menor.


POR QUE FLASH-TSDB

Problema Común                      Solución Flash-TSDB
----------------------------------  ----------------------------------------
SQLite destruye tarjetas SD         Escritura secuencial (append-only)
InfluxDB requiere GB de RAM         Funciona con menos de 2 MB de RAM
Logs de texto son lentos            Formato binario de 20 bytes
Sin queries sobre datos comprimidos Motor de consultas nativo
Sin agregaciones estadísticas       Min/Max/Avg/Sum/Count por bucket


RENDIMIENTO

Metricas Clave:

- Throughput de insercion: 240,000 puntos/segundo
- Tamano por registro:     20 bytes (binario puro)
- Compresion en disco:     70% (LZ4HC)
- Consulta indexada:       0.12 ms (40K puntos)
- Construccion de indice:  0.08 ms
- Memoria del indice:      1.56 KB (40 bloques)
