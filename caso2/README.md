La intención es mejorar la comprension del comportamiento al definir varias HTTPRoute con el mismo hostname y diferentes AuthPolices.
Probado en Conn Link/Kuadrant 1.4

Revisar los Manifiesto y realizar ajustes según cluster destino en valor como hostname.

curl -kv "http://api.fortaleza.bank:80/" -H'app_id: a8d4c529' -H'app_key: secretValue'

curl -kv "http://api.fortaleza.bank:80/v1" -H'app_id: 731b0759' -H'app_key: password'
