# Programación de servicios y procesos: Plataforma para ofertar empleo (Ejercicio final)

**Backend** para el ejercicio 2 de Programación de Servicios y Procesos.

## Que vas a encontrar aquí

* Este repositorio genera una API REST, creada con JHipster (Spring Boot)
* Si no quieres montarte esta API, la tienes disponible
  en: [https://cev-psp-ej2-back.herokuapp.com/](https://cev-psp-ej2-back.herokuapp.com/). Obviamente, si pinchas el link
  te mostrará _Your request cannot be processed_, recuerda que esto es un API rest.
* Puedes probar [importando en Postman](https://learning.postman.com/docs/getting-started/importing-and-exporting-data/)
  el fichero `PSP-EJ2-EXPORT.postman_collection.json` que se encuentra en la raíz de este repositorio.

### Documentación

#### Listado de ofertas ([`https://cev-psp-ej2-back.herokuapp.com/api/ofertas`](`https://cev-psp-ej2-back.herokuapp.com/api/ofertas`))

* Método: GET
* Auth: No
* Entrada: N/A
* Salida:

```json
[
  {
    "id": 1,
    "titulo": "Buckinghamshire",
    "descripcion": "forecast",
    "empresa": "Developer Hong Kong Dollar synthesize",
    "salario": 58479,
    "ciudad": "Nepal Human array",
    "email": "Madge_Mayert@hotmail.com"
  }
]
  ```

#### Detalle de oferta ([`https://cev-psp-ej2-back.herokuapp.com/api/ofertas/1`](`https://cev-psp-ej2-back.herokuapp.com/api/ofertas/1`))

* Método: GET
* Auth: No
* Entrada: N/A
* Salida:

```json
{
  "id": 1,
  "titulo": "Buckinghamshire",
  "descripcion": "forecast",
  "empresa": "Developer Hong Kong Dollar synthesize",
  "salario": 58479,
  "ciudad": "Nepal Human array",
  "email": "Madge_Mayert@hotmail.com"
}
  ```

#### Autenticación ([`https://cev-psp-ej2-back.herokuapp.com/api/authenticate`](`https://cev-psp-ej2-back.herokuapp.com/api/authenticate`))

* Método: POST
* Auth: No
* Entrada:

```json
{
  "username": "admin",
  "password": "admin",
  "rememberMe": "false"
}
  ```

* Salida:

```json
{
  "id_token": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJhZG1pbiIsImF1dGgiOiJST0xFX0FETUlOLFJPTEVfVVNFUiIsImV4cCI6MTYzNjEyOTA4Mn0.1zlwA7XkDIbvDJd_gTe7RVR6MGi2DiBCEIV5BuTQT-Km5hNKuZ7qQF7TmbJoxmaHT0Mi1aubvYrBl6r6zqC6rw"
}
  ```

#### Insertar nueva oferta ([`https://cev-psp-ej2-back.herokuapp.com/api/ofertas`](`https://cev-psp-ej2-back.herokuapp.com/api/ofertas`))

* Método: POST
* Auth: Bearer token
* Entrada:

```json
{
  "titulo": "Buckinghamshire",
  "descripcion": "forecast",
  "empresa": "Developer Hong Kong Dollar synthesize",
  "salario": 58479,
  "ciudad": "Nepal Human array",
  "email": "Madge_Mayert@hotmail.com"
}
  ```

* Salida:

```json
{
  "id": 998876,
  "titulo": "Buckinghamshire",
  "descripcion": "forecast",
  "empresa": "Developer Hong Kong Dollar synthesize",
  "salario": 58479,
  "ciudad": "Nepal Human array",
  "email": "Madge_Mayert@hotmail.com"
}
  ```

#### Eliminar oferta ([`https://cev-psp-ej2-back.herokuapp.com/api/ofertas/1`](`https://cev-psp-ej2-back.herokuapp.com/api/ofertas/1`))

* Método: DELETE
* Auth: Bearer token
* Entrada: N/A
* Salida:

```json
{
  "id": 1,
  "titulo": "Buckinghamshire",
  "descripcion": "forecast",
  "empresa": "Developer Hong Kong Dollar synthesize",
  "salario": 58479,
  "ciudad": "Nepal Human array",
  "email": "Madge_Mayert@hotmail.com"
}
```
