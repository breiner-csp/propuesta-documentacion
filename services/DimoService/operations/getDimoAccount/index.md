[<-- Volver al listado de operaciones](./../../index.md)

# Dimo Service / getDimoAccount

###  Esta operación permite consultar a través del proveedor Praxis, si un número de teléfono está vinculado a una cuenta CLABE en la base de datos de Banxico para realizar transferencias Dimo.
---


## Tabla de control de cambios
|Responsable|Historia de usuario|Descripción del cambio|
|-|-|-|
|exbhgarcia|[86b1x64g2](https://app.clickup.com/t/86b1x64g2)|Se adiciona la operación al servicio|

---


## Diagrama de componentes
![Diagrama de componentes](./img/components.png)

---


## Request Body
```
{
  "getDimoAccountRequestBO": {
    "applicationId": "string",
    "cellphoneNumber": "string"
  }
}
```
## Especificación de objetos y atributos del Request


---

## Response Body
```
{
  "getDimoAccountResponseBO": {
    "status": "string",
    "code": "string",
    "response": "string",
    "data": {
      "recordFound": false,
      "maskedCustomerName": "string",
      "accountType": "string",
      "accountNumber": "string",
      "claveSPEI": "string",
      "rfc": "string",
      "folioPet": "string"
    }
  }
}
```
## Especificación de objetos y atributos del Response


---

## Estados de respuesta

---
## Códigos de respuesta


---


## URL de API por ambiente
|Ambiente|URL|
|-|-|
|Desarrollo|https://apic.consubanco.com/csb/dev/dimo-service/getDimoAccount|    
|Calidad|https://apic.consubanco.com/csb/qa/dimo-service/getDimoAccount|
|Producción|https://apic.consubanco.com/csb/prd/dimo-service/getDimoAccount|

---


## Ejemplo de consumo del API - cURL
```
curl --location 'https://apic.consubanco.com/csb/dev/dimo-service/getDimoAccount' \
--header 'Content-Type: application/json' \
--header 'Accept: application/json' \
--header 'X-IBM-Client-Id: 1045c7b96ff237918538c15ffecbc8dd' \
--header 'Cookie: 0f64ea607ea127be876814b5b38b0d94=c6c8f20ec97961f1e06618f4e1fd07e1' \
--data 'REPLACE_REQUEST_BODY'
```
---


## Componentes de integración relacionados
|Componente|Paquete/Clase|Método|
|-|-|-|
|int-esb-rest-services-mdw|com.consubanco.rest.dimo.impl.DimoServicesImpl|getDimoAccount|

---
## Componentes externos relacionados
|Tipo|Método|URL|Headers|
|-|-|-|-|
|REST|POST|http://csbsamdint1.consupago.com:9080/karpaydm/api/banxico/consulta|X-API-KEY<br>X-API-SECRET|

---

## Mapeos
## Request: Integración ---> Praxis
![Request a praxis](./img/map-request.png)
## Response Praxis ---> Integración
![Request a praxis](./img/map-response.png)

---