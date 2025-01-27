[<-- Volver al listado de operaciones](./../../index.md)

# Karalundi Service / getSignedDocument

###  Esta operación consulta un documento firmado
---

## Tabla de control de cambios
|Responsable|Historia de usuario|Versión de API donde se aplica el cambio|Descripción del cambio|
|-|-|-|-|
|exbhgarcia|[86b37vbza](https://app.clickup.com/t/86b37vbza)|v1.0.0|Se adiciona la operación al servicio|

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
  "getSignedDocumentRequestBO": {
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
|getSignedDocumentRequestBO|GetSignedDocumentRequestBOObject|M|1|255|V|

* ### GetSignedDocumentRequestBOObject
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
  "getSignedDocumentResponseBO": {
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
|getSignedDocumentResponseBO|GetSignedDocumentResponseBOObject|

* ### GetSignedDocumentResponseBOObject
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
|Desarrollo|https://apic.consubanco.com/csb/dev/karalundi-service/getSignedDocument|    
|Calidad|https://apic.consubanco.com/csb/qa/karalundi-service/getSignedDocument|
|Producción|https://apic.consubanco.com/csb/prd/karalundi-service/getSignedDocument|

---


## Ejemplo de consumo del API - cURL
```
curl --location 'https://apic.consubanco.com/csb/dev/karalundi-service/getSignedDocument' \
--header 'Content-Type: application/json' \
--header 'Accept: application/json' \
--header 'X-IBM-Client-Id: XXXXXXXXXXXXXXXXX' \
--header 'Cookie: 0f64ea607ea127be876814b5b38b0d94=c6c8f20ec97961f1e06618f4e1fd07e1' \
--data 'REPLACE_REQUEST_BODY'
```
---


<!-- DOCUMENTACION TECNICA -->
## Diagrama de componentes
![Diagrama de componentes](./img/components.png)

---

## Componentes de integración relacionados
|Componente|Paquete/Clase|Método|
|-|-|-|
|shermfin-ws|mx.com.karalundi.impl.KaralundiImpl|getSignedDocument|

---

## Componentes externos relacionados
|Tipo|Método|URL|
|-|-|-|
|SOAP|POST|https://wstestautosign.doc2sign.com/Doc2SignLite.svc|

---

## Mapeos
## Request: Integración ---> Karalundi
![Mapeo de request](./img/map-request.png)
## Response: Karalundi ---> Integración
![Mapeo de response](./img/map-response.png)

---


