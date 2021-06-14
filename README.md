# Javascript.timer

Un temporizador que puede ser pausado, elegir la duracion, terminarlo, cambiarle la velocidad si es necesario, modificar un texto final y que hace un ruido al terminar el tiempo
para avisarte si es que no quieres tenerlo todo el tiempo maximizado en tu pantalla!


  EXPLICACION DEL PROYECTO

  Lineas 1 - 32

                    Creamos todas las variables que usaremos, extrayendo la mayoria de elementos HTML.

  Lineas 35 - 69

                    Dentro de la funcion de configurar el temporizador:
                    Creamos una funcion para parar la cuenta atras, y funciones para habilitar o deshabilitar botones.

  Lineas 70 - 75

                    Empezamos por desactivar el boton de configurar, ya que fue presionado.

  Linea 76 - 92

                    Creamos un prompt para preguntarle al usuario de cuantos minutos desea que sea su Temporizador
                    A este numero le restamos un 1.

                    ¿Por que? Porque los segundos automaticamente empezaran desde 59, y si elejimos 5 minutos y no le restamos un 1 minuto,
                    el contador figurara como 5:59 en vez de 4:59 minutos.

                    Creamos un intervalo de 60 segundos, donde cada vez que pasen 60 segundos, el contador de minutos baje 1 unidad.

                    Creamos un condicional, donde si minutos llega a -1, significa que la cuenta atras ya ha terminado, y se frena todo en 0.


  Linea 95 - 116

                    Definimos segundos para que automaticamente empiecen valiendo 59.

                    Creamos un intervalo de 1 segundo, para que el contador de segundos baje una unidad cada segundo.

                    Para que al llegar a 0 segundos vuelva a valer 60 y no siga bajando en negativo, se crea un condicional:

                        "Si segundos es igual a 0, asignarle el valor 60."

                    Pero tambien se crea otra condicion, que:

                        "Si minutos es igual a -1, entonces significa que ya no deberia seguir funcionando la cuenta atras y que el contador ha
                        llegado a su fin. Se procede a: parar los intervalos de segundos y minutos, hacer sonar un audio, habilitar el boton de
                        configurar para poder iniciar otro cronometro, etc."


   Linea 119 - 127

                    Al apretar el boton de parar, que se reemplace el boton de parar por el de reanudar, que se frene el conteo y que se habilite
                    el boton de configurar.


  Linea 130 - 140


                    Al apretar el boton de reanudar, se crea una funcion que se reemplace el de Reanudar por el de Terminar.
                    Como al reanudarse se inicia un conteo nuevo, deshabilitamos el boton de configurar.

  Linea 140 - 156

                    Se crea un intervalo nuevo al reanudar, donde se toman los segundos y minutos que ya estaban frenados en el conteo anterior
                    A diferencia del primer intervalo, en este solamente van a bajar los numeros, y al llegar los segundos a 0, volveran a 60
                    y los minutos bajaran 1.

                    Pero si minutos y segundos, ambos son iguales a 0, entonces el boton de terminar se reemplazara por el de parar (asi se prepara para un proximo intervalo)
                    Tambien se frenara el intervalo, se habilitara el boton de configurar, y sonara el audio.

  Linea 158 - 167


                    Al apretar el boton de terminar, se limpiaran los intervalos, se setearan los segundos y minutos a 0, se habilitaran
                    los botones PARAR y CONFIGURAR, desaparecera el boton de Terminar.


  Linea 175 - 194


                    Al clickear los botones de cerrar o abrir el modal, tan solo se cambiara el display de este, intercalando entre "block" y "none".
                    Tambien al apretar el boton en el modal de modificar el texto final, se recojera la respuesta en un prompt.
