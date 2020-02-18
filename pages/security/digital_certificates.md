---
title: Certificados digitales
tags: [security, network_security, digital_certificates]
keywords:
summary: "This posts will be written in spanish, because scholar necessities."
sidebar: security_sidebar
permalink: digital_certificates.html
folder: security
---

## Certificados digitales

### ¿Qué es?
Básicamente un certificado digital es un documento digital que se vincula a la identidad de una persona o entidad, la cual es garantizada por una Tercera Parte Confiable(Autoridad de certificación).

### ¿Qué partes componen un certificado digital?

-  La identidad de su propietario.
-  El ámbito de utilización. 
-  Las fechas de inicio y fin de validez del certificado
-  Una serie de campos adicionales que identifican al certificado, que carecen de importancia para el presente artículo.
-  Una  clave  privada,  que  únicamente  la  posee  el  propietario.  Esta  es    un  complicado   algoritmo   matemático,   cuyo   acceso   está   protegido   por   una   contraseña (PIN).
-  Una  clave  pública,  que  es  conocida  y  publicada  en  la  Web  por  la  Autoridad certificadora,  tras  su  aprobación,  y  que  es  firmada  con  su  clave  privada  (conocida  como  Clave  Privada Raiz). Al igual que la clave privada, es un complicado algoritmo, el cual tiene la peculiaridad de que es capaz de descrifrar un mensaje encriptado con la clave privada, y viceversa. 

### ¿Qué me asegura el certificado digital? 

*  Autenticación. Como  mencionamos  anteriormente,  el  certificado  se  asocia  con  una única identidad. 
*  Confidencialidad. Es posible encriptar una información para que únicamente la lea  el  usuario  seleccionado.  Gracias  a  ello,  si  un  tercer  elemento  intercepta  el  mensaje  al  viajar  por  una  red  no  segura  (Internet),  no  podrá  descrifar  el  mensaje.
*  Integridad.  El  receptor  de  un  mensaje  podrá  comprobar  si  en  el  envío  se  ha  corrompido   o   modificado   intencionadamente   por   un   tercer   elemento,   y   corresponde exactamente al mensaje enviado por el emisor. 
*  No repudio en origen. Esto implica que un mensaje siempre podrá ser asociado al usuario que lo remitió.
