---
title: Firma digital
tags: [security, network_security, digital_sign]
keywords:
summary: "This posts will be written in spanish, because scholar necessities."
sidebar: security_sidebar
permalink: digital_sign.html
folder: security
---

## Firma digital(FIEL)

### ¿Qué es?
A grandes rasgos la firma electronica avanzada contiene codigos y elementos unicos hechos para avalar tu identidad.

### ¿Qué archivo me da el SAT para que mi FIEL funcione?

 

``` 

*  Archivo con terminación .cer (certificado)
*  Archivo con terminación .key (llave)

```

## Teoria detras de una firma digital

### ¿Qué es una firma digital?
Es una firma, que a traves de un certificado digital emitido por una entidad certificadora(Ejemplot: SHCP)
incorpora una seri de datos electronicos que te identifican como firmante a con la ayuda de un proceso de
criptografia.

### Pasos que se llevan a cabo para validar a un firmante con la ayuda de una firma digital

Para explicar este procedimiento tomaremos como punto de inicio el siguiente escenario:

Un usuario que podria se usted, desea enviar una factura electronica, el usuario cuenta con su certificado y su llave
que mencionamos algunos parrafos mas arriba.

``` 

1.  El usuario carga su firma y su cetificado en la aplicación del SAT.
2.  El usuario da click en enviar.
3.  La aplicacion del SAT envia una copia de la factura electronica en conjunto con la llave y el 

certificado.

4.  El siguiente proceso se lleva a cabo al mismo tiempo, con la copia cargada en la coputadora del 

cliente y la copia que se ha enviado al SAT.

  + La factura electronica mediante una funciona hash(Entra una serie de caracteres con sentido legible y sale una serie de caractres sin un sentido legible) se convierte en una huella digital.

5.  La huella digital resultante en la computadora del usuario es cifrada(pasa de algo comprensible a algo incomprensible) y enviada al SAT
6.  La huella digital ya en el SAT, es descifrada(de algo incomprensible a algo comprensible) y se compara con la huella digital que se genera en el SAT para verficar que durante el envio no haya existido alguna alteración y tambien confirmar la identidad del que envia la factura.


```
### Esquema detallado y tecnico de la firma digital
{% include image.html file="firma.png" url="http://jekyllrb.com" alt="Jekyll" caption="Esquema detallado y tecnico de la firma digital" %}



