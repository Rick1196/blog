---
title: Certificados digitales
tags: [security, network_security, encryptation, sha]
keywords:
summary: "This posts will be written in spanish, because scholar necessities."
sidebar: security_sidebar
permalink: sha.html
folder: security
---

## SHA

### ¿Qué es?
    SHA, que significa algoritmo hash seguro, es un algoritmo hash utilizado por las autoridades de certificación para firmar certificados y CRL (lista de revocación de certificados). Introducido en 1993 por NSA con SHA0, se utiliza para generar valores hash únicos a partir de archivos.

    Ejemplo: un archivo hash con SHA1 podría verse así:
    752c14ea195c369bac3c3b7896975ee9fd15eeb7

    En cuanto a cualquier solución criptográfica, SHA debe evolucionar junto con las capacidades de cálculo de nuestras computadoras para evitar cualquier debilidad.

    Hay, por lo tanto, varias versiones de SHA: SHA0 (obsoleto), SHA1 (Obsoleto), SHA2 y finalmente SHA3 introducido en 2012.

### SHA1
    SHA-1 es un algoritmo que produce una huella digital de 160 bits cuando se usa en un mensaje.

    Era el estándar hasta ahora para las conexiones seguras. Sin embargo, SHA-1 se adoptó en 1995, hace mucho tiempo en internet. ¡Solo piense en la computadora que estaba usando en 1995! Grandes avances en tecnología y desarrollos en criptografía desde entonces están presionando a SHA-1, y se ha demostrado que no es confiable.

    Sus días están contados y la industria SSL está migrando a SHA-2. A partir del 1 de enero de 2017, los navegadores web y los sistemas operativos dejarán de reconocer los certificados SSL que utilizan SHA-1, lo que los hará inútiles. La mayoría de los principales navegadores (Chrome, Safari, Mozilla, Opera) han expresado su apoyo al movimiento.

#### ¿Cómo funciona SHA-2?
    SHA-2 es un conjunto de funciones hash de criptografía que funcionan con múltiples algoritmos hash. Incluye múltiples variaciones de funciones hash criptográficas como SHA-224, SHA-256 (la más popular), SHA-384, SHA-512, SHA-512/224, SHA-512/256. La investigación sobre este nuevo algoritmo SHA-2 realizada por expertos en seguridad muestra que es casi imposible romper esta estructura de múltiples funciones hash y debería ser completamente segura en el futuro previsible.

    SHA-2 es un mecanismo matemático. Utiliza un algoritmo unidireccional para producir una cadena que es única para cada archivo. Esta cadena, llamada hash, es una longitud de bits establecida (basada en la función SHA específica elegida, la más popular de estas, SHA-256 es de 256 bits. El número que sigue a cada una de las funciones denota su longitud de bits). Por lo tanto, cada archivo del que se tome un hash SHA-2556 tendrá un valor hash único de igual longitud. La naturaleza unidireccional de esta función significa que si le dan un hash, no puede usarlo para recrear o determinar cuál era el archivo original. Cuando un proveedor SSL lo valida para un certificado, almacena el valor hash de su certificado específico y se distribuye con su certificado. Luego se utiliza para validar la autenticidad de su certificado cuando un cliente (el navegador de un usuario) se conecta a su servidor.

#### ¿Cómo obtengo un certificado SHA-2?
    Para obtener un certificado SHA-2, primero debe elegir un proveedor SSL que sea capaz de suministrar certificados firmados por SHA-2. Hemos investigado el mercado y documentado las principales marcas que firman certificados con SHA-2. Estas marcas son Symantec, GeoTrust, Thawte, RapidSSL y Comodo.

        -  Symantec ya ha migrado toda su línea de productos de certificados SSL y Certificados de firma de código al algoritmo SHA-2 y tuvieron un anuncio oficial en el blog.
        -  GeoTrust y RapidSSL han agregado recientemente soporte para SHA-2 en sus paneles para todos sus certificados.
        -  Comodo ha admitido el algoritmo SHA-2 durante un tiempo y ahora lo ha convertido en su configuración predeterminada para todos los certificados SSL.
        -  Thawte ya ha tenido toda su cartera de certificados SSL para el algoritmo SHA-2 más fuerte y ya han comenzado a emitir certificados basados ​​en SHA-2 a sus clientes.

    Si ya tiene un certificado actual de una de estas marcas u otra CA que proporciona certificados SHA-2, entonces todo lo que necesita hacer es volver a emitir su certificado actual y solicitar que se firme con el algoritmo SHA-2. Con las marcas anteriores, esto se realiza durante su proceso de inscripción y no es necesario especificar SHA-2 en su CSR.

    Si su proveedor SSL actual no ofrece certificados SHA-2, o si aún no tiene un certificado SSL, puede comprar un nuevo certificado de un proveedor que suministre marcas con soporte SHA-2.




