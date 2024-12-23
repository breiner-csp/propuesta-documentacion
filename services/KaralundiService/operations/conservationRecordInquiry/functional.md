[<-- Volver al listado de operaciones](./../../index.md)

# Karalundi Service / conservationRecordInquiry

###  Esta operación consulta la constancia de conservación
---

## Tabla de control de cambios
|Responsable|Historia de usuario|Versión de API donde se aplica el cambio|Descripción del cambio|
|-|-|-|-|
|exbhgarcia|[86b37vbzc](https://app.clickup.com/t/86b37vbzc)|v1.0.0|Se adiciona la operación al servicio|

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
  "conservationRecordInquiryReqBO": {
    "applicationId": "string",
    "credential": {
      "userService": "string",
      "passwordService": "string",
      "identifier": "string"
    }
  }
}
```
## Especificación de objetos y atributos del Request
* ### Request Body
| Campo | Tipo | M/O | L/Mi | L/Ma | V/C |
|-|:-:|:-:|:-:|:-:|:-:|
|conservationRecordInquiryReqBO|ConservationRecordInquiryReqBOObject|M|1|255|V|

* ### ConservationRecordInquiryReqBOObject
| Campo | Tipo | M/O | L/Mi | L/Ma | V/C |
|-|:-:|:-:|:-:|:-:|:-:|
|applicationId|String|M|1|255|V|
|credential|CredentialObject|M|1|255|V|

* ### CredentialObject
| Campo | Tipo | M/O | L/Mi | L/Ma | V/C |
|-|:-:|:-:|:-:|:-:|:-:|
|userService|String|M|1|255|V|
|passwordService|String|M|1|255|V|
|identifier|String|M|1|255|V|

---

## Response Body
```
{
  "conservationRecordInquiryRespBO": {
    "status": "string",
    "code": "string",
    "response": "string",
    "base64": "string"
  }
}
```
## Especificación de objetos y atributos del Response
* ### Response Body
| Campo | Tipo |
|-|:-:|
|conservationRecordInquiryRespBO|ConservationRecordInquiryRespBOObject|

* ### ConservationRecordInquiryRespBOObject
| Campo | Tipo |
|-|:-:|
|status|String|
|code|String|
|response|String|
|base64|String|

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
|Desarrollo|https://apic.consubanco.com/csb/dev/karalundi-service/conservationRecordInquiry|    
|Calidad|https://apic.consubanco.com/csb/qa/karalundi-service/conservationRecordInquiry|
|Producción|https://apic.consubanco.com/csb/prd/karalundi-service/conservationRecordInquiry|

---


## Ejemplo de consumo del API - cURL
```
curl --location 'https://apic.consubanco.com/csb/dev/karalundi-service/conservationRecordInquiry' \
--header 'Content-Type: application/json' \
--header 'Accept: application/json' \
--header 'X-IBM-Client-Id: XXXXXXXXXXXXXXXXX' \
--header 'Cookie: 0f64ea607ea127be876814b5b38b0d94=c6c8f20ec97961f1e06618f4e1fd07e1' \
--data 'REPLACE_REQUEST_BODY'
```
---

