# Enunciado: Mobile World Congress (diagrama E/R)

Hay que hacer el diagrama Entidad-Relación de este enunciado.

---

En Barcelona todos los años se realiza el Mobile World Congress, la conferencia de tecnología móvil más grande del mundo. Este año la organización nos ha pedido ayuda para organizar la próxima conferencia.

En esta Conferencia las compañías muestran sus nuevos productos. De cada compañía deseamos almacenar, su nombre (que es único), el año de fundación, su presidente y el capital que maneja la empresa.

Cada compañía como mínimo envía un representante, pero puede enviar más de uno. De los representantes deseamos saber su número de pasaporte, el nombre y el país. Los representantes siempre pertenecen a alguna compañía, ahora bien, tiene exclusividad, así que no pueden pertenecer a otra.

Las compañías se dedican a promocionar todos sus dispositivos. De ellos, nos interesa saber el nombre (que es único), el tipo de dispositivo (móvil, app, auriculares, etc.), una descripción, la fecha de lanzamiento y el precio.

Las compañías se ubican en stands, cada stand está identificado por un número único en toda la MWC, tiene una ubicación y un tamaño en metros cuadrados. Una compañía puede utilizar más de un stand, pero también hay compañías más pequeñas que pueden usar el mismo stand. Todos los stands están siendo usados por alguna compañía. Como es evidente, todas las compañías deben estar ubicadas en algún stand.

El Mobile dispone de una serie de Salas para realizar las presentaciones de los diversos productos. Cada Sala tiene un nombre (que es único), una ubicación y una determinada capacidad. Cada compañía puede realizar varios eventos y en diversas salas. Del evento nos interesa almacenar el nombre y categoría.

Es importante saber la fecha que se realiza el evento de una compañía en concreto y en qué sala y que presentador. Un mismo día se pueden realizar varios eventos en una misma sala.

Por ejemplo: Samsung realiza en la sala Magma el evento Presentación el 20/12/2026 con el presentador A, pero Samsung en la sala Magma el evento I+D lo realiza el presentador B.
También Xiaomi, en la sala Magma el evento Presentación el 21/12/2026 puede hacerlo el presentador Z.

Nos interesa almacenar los periodistas que asisten a un determinado evento. No importa la compañía ni sala. Todo evento asiste un mínimo de 1 periodista y un máximo de 50. Un periodista puede asistir a más de un evento. Los periodistas los identificamos por su número de pasaporte, pero debemos conocer también, su nombre y apellido, fecha nacimiento y la edad que viene determinada por su fecha de nacimiento.

Existen empresas que participan como patrocinadores en los eventos para realizar publicidad, por ejemplo, Coca-Cola. De cada una de estas empresas deseamos saber, su nombre (que es único), su nombre de presidente y el país al que pertenece.

Cada empresa patrocina como mínimo un evento, pero puede patrocinar más. Cada evento como mínimo tiene un patrocinador. Estas empresas patrocinan con un importe a los eventos, que no es el mismo en cada evento. Por ejemplo, Coca-Cola patrocina con 50.000€ al evento I+D, pero Coca-Cola también puede patrocinar al evento Presentación, pero con 20.000€.
