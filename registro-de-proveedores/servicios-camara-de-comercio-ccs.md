# Servicios Cámara de Comercio \(CCS\)

{% api-method method="post" host="https://api.mercadopublico.cl" path="/v1/proveedor/registro" %}
{% api-method-summary %}
Actualiza Registro Persona
{% endapi-method-summary %}

{% api-method-description %}
Servicio web que actualiza los datos del usuario. Se debe realizar también en la CCS para mantener datos actualizados.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="codigo" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="rut" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="nombres" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="apellidos" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="telefono" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="contrasena" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "codigo": 200,
    "message": "Persona registrada satisfactoriamente."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "codigo": 404,
    "message": "La persona no pudo registrarse."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

