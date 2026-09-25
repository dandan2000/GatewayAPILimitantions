La intención es mejorar la comprension del comportamiento al definir dos AuthPolicies referenciando el mismo HTTPRoute.
Probado en Conn Link/Kuadrant 1.4

Revisar los Manifiesto y realizar ajustes según cluster destino en valor como hostname.

oc get authpolicy -o wide  -n limitations-1

NAME             ACCEPTED   ENFORCED   TARGETKIND   TARGETNAME   TARGETSECTION   AGE

auth-static-p1   True       True       HTTPRoute    fake-api                     59s

auth-static-p2   True       False      HTTPRoute    fake-api                     63s


La prueba concluye que la mas "joven" queda como activa (Enforced) en cambio la otra queda como Overridden.

message: 'AuthPolicy is overridden by [limitations-1/auth-static-p1]'


Contradiciendo la especificación estándar de Gateway API (GEP-713 / Policy Attachment) para la resolución de conflictos al mismo nivel jerárquico que indica que prevalece y queda adjunta la más VIEJA (la que tenga el creationTimestamp más antiguo).

auth-static-p1 (Más nueva): Creada a las 19:29:04Z

auth-static-p2 (Más vieja): Creada 4 segundos antes, a las 19:29:00Z
