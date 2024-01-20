# problema-barberos

En una peluquería hay barberos y sillas para los clientes (siempre hay más sillas que clientes). Sin embargo, en esta peluquería no siempre hay trabajo por lo que los barberos duermen cuando no hay clientes a los que afeitar. Un cliente puede llegar a la barbería y encontrar alguna silla libre, en cuyo caso, el cliente se sienta y esperará que algún barbero le afeite. Puede ocurrir que el cliente llegue y no haya sillas libres, en cuyo caso se marcha. Simular el comportamiento de la barbería mediante un programa Java teniendo en cuenta que:

Se generan clientes continuamente, algunos encuentran silla y otros no. Los que no consigan silla desaparecen (terminan su ejecución)

Puede haber más sillas que barberos y al revés (poner constantes para poder cambiar fácilmente entre ejecuciones).

Se recuerda que no debe haber inanición, es decir ningún cliente debería quedarse en una silla esperando un tiempo infinito.

## Solución 1 Barberos dormilones
El problema está en que la forma que tiene el gestor de concurrencia de decirle a un barbero qué silla tiene un cliente sin afeitar es incorrecta: como siempre se empieza a buscar por el principio del vector, los clientes sentados al final nunca son atendidos. Hay que corregir esa asignación para evitar que los procesos sufran de inanición.


