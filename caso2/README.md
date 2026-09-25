La intención es mejorar la comprension del comportamiento al definir varias HTTPRoute con el mismo hostname y diferentes AuthPolices.
Probado en Conn Link/Kuadrant 1.4

Revisar los Manifiesto y realizar ajustes según cluster destino en valor como hostname.

curl -kv "http://api.fortaleza.bank:80/" -H'app_id: a8d4c529' -H'app_key: secretValue'

curl -kv "http://api.fortaleza.bank:80/v1" -H'app_id: 731b0759' -H'app_key: password'


La prueba concluye que el comportamiento es el esperado, funcionan ambas Policies. 
Pero es importante destacar que frente a repeticiones de hostname + path (que es posible si diferentes personas editan los HTTPRoute), el primero de ellos será el utilizado y el resto no recibirán tráfico sin ninguna advertencia.

