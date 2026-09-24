La intención es mejorar la comprension del comportamiento al definir mas de 64 listener para un Gateway
Probado en Conn Link/Kuadrant 1.4

oc apply -f  gateway-limit-test.yaml

The Gateway "limit-test-gateway" is invalid:
* spec.listeners: Too many: 65: must have at most 64 items
* <nil>: Invalid value: null: some validation rules were not checked because the object was invalid; correct the existing errors to complete validation
