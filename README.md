## Pruebas prácticas que documentan Limitaciones de Gateway API y componentes de Connectivity Link / Kuadrant

Antes de aplicar revisar si los hostnames definidos deben actualizarse de acuerdo al cluster destino.

Pruebas realizadas sobre Connectivity Link 1.4 sobre Istio 1.30.x

[Dos AuthPolicies referenciando el mismo HTTPRoute](caso1/README.md)

[Dos HTTPRoute con el mismo hostname y diferentes AuthPolices](caso2/README.md)

[Mas de 64 listener para un Gateway](caso3/README.md)
