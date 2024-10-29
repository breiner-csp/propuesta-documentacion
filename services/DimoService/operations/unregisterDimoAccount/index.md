[<-- Volver al listado de operaciones](./../../index.md)

# Dimo Service / unregisterDimoAccount

###  Esta operación permite consultar a través del proveedor Praxis, si un número de teléfono está vinculado a una cuenta CLABE en la base de datos de Banxico para realizar transferencias Dimo.
---


## Tabla de control de cambios
|Responsable|Historia de usuario|Versión de API donde se aplica el cambio|Descripción del cambio|
|:-:|:-:|:-:|-|
|exbhgarcia|[86b1x6en7](https://app.clickup.com/t/86b1x6en7)|v1.0.0|Se adiciona la operación al servicio|

---


## Diagrama de componentes
![Diagrama de componentes](./img/components.png)

---


## Simbología y convenciones
|Símbolo - Convención|Descripción|
|-|-|
|Campo|Indica el nombre del atributo|
|Tipo|Indica el tipo de dato del atributo|
|M|Campo mandatorio o requerido|
|O|Campo opcional|
|L/Mi|Longitud mínima|
|L/Ma|Longitud Máxima|
|V/C|Indica si es variable o constante|
|N/A|No aplica|
|N/E|No especificado|


## Request Body
```
{
  "unregisterDimoAccountRequestBO": {
    "applicationId": "string",
    "cellphoneNumber": "string"
  }
}
```
## Especificación de objetos y atributos del Request
* ### Request Body
| Campo | Tipo | M/O | L/Mi | L/Ma | V/C |
|-|:-:|:-:|:-:|:-:|:-:|
|unregisterDimoAccountRequestBO|UnregisterDimoAccountRequestBOObject|M|1|255|V|

* ### UnregisterDimoAccountRequestBOObject
| Campo | Tipo | M/O | L/Mi | L/Ma | V/C |
|-|:-:|:-:|:-:|:-:|:-:|
|applicationId|String|M|1|255|V|
|cellphoneNumber|String|M|1|255|V|


---

## Response Body
```
{
  "unregisterDimoAccountResponseBO": {
    "status": "string",
    "code": "string",
    "response": "string",
    "data": {
      "folioPet": "string"
    }
  }
}
```
## Especificación de objetos y atributos del Response
* ### Request Body
| Campo | Tipo |
|-|:-:|
|unregisterDimoAccountResponseBO|UnregisterDimoAccountResponseBOObject|

* ### UnregisterDimoAccountResponseBOObject
| Campo | Tipo |
|-|:-:|
|status|String|
|code|String|
|response|String|
|data|DataObject|

* ### DataObject
| Campo | Tipo |
|-|:-:|
|folioPet|String|

---

## Estados de respuesta
|Estado|Descripción|
|:-:|-|
|C|Transacción exitosa|
|E|Transacción errónea|

---
## Códigos de respuesta
|Código|Descripción|
|:-:|-|
|200|Transacción exitosa|
|301|Solicitud con errores|
|500|Error interno|

---


## URL de API por ambiente
|Ambiente|URL|
|-|-|
|Desarrollo|https://apic.consubanco.com/csb/dev/dimo-service/unregisterDimoAccount|    
|Calidad|https://apic.consubanco.com/csb/qa/dimo-service/unregisterDimoAccount|
|Producción|https://apic.consubanco.com/csb/prd/dimo-service/unregisterDimoAccount|

---


## Ejemplo de consumo del API - cURL
```
curl --location 'https://apic.consubanco.com/csb/dev/dimo-service/unregisterDimoAccount' \
--header 'Content-Type: application/json' \
--header 'Accept: application/json' \
--header 'X-IBM-Client-Id: XXXXXXXXXXXXXXXXX' \
--header 'Cookie: 0f64ea607ea127be876814b5b38b0d94=c6c8f20ec97961f1e06618f4e1fd07e1' \
--data 'REPLACE_REQUEST_BODY'
```
---


## Componentes de integración relacionados
|Componente|Paquete/Clase|Método|
|-|-|-|
|int-esb-rest-services-mdw|com.consubanco.rest.dimo.impl.DimoServicesImpl|unregisterDimoAccount|

---
## Componentes externos relacionados
|Tipo|Método|URL|Headers|
|-|-|-|-|
|REST|POST|http://csbsamdint1.consupago.com:9080/karpaydm/api/banxico/baja|X-API-KEY<br>X-API-SECRET|

---

## Mapeos
## Request: Integración ---> Praxis
![Request a praxis](./img/map-request.png)
## Response Praxis ---> Integración
![Request a praxis](./img/map-response.png)

---