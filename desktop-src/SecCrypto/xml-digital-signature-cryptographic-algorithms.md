---
description: Криптксмл изначально поддерживает указанные ниже URI.
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: Алгоритмы шифрования цифровых подписей XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290be3708565cf144b5bf23bfcb1ddfe5252b227c12bbcebbd81b68d0fc2df07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895790"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a>Алгоритмы шифрования цифровых подписей XML

Криптксмл изначально поддерживает указанные ниже URI. Если для криптографических алгоритмов и преобразований, которые не являются частью встроенной поддержки, требуется поддержка, вы можете использовать криптографические [криптографические расширения](xml-digital-signature-cryptographic-extensions.md) [следующего поколения](../seccng/cng-portal.md) и XML для поддержки новых алгоритмов.

## <a name="supported-uris"></a>Поддерживаемые URI

Методы дайджеста



| Константа                                 | Значение URI                                                   |
|------------------------------------------|-------------------------------------------------------------|
| Всзури \_ xmlns \_ дигсиг \_ SHA1<br/>   | "https://www.w3.org/2000/09/xmldsig\#sha1"<br/>        |
| Всзури \_ xmlns \_ дигсиг \_ SHA256<br/> | "https://www.w3.org/2001/04/xmlenc\#sha256"<br/>       |
| Всзури \_ xmlns \_ дигсиг \_ SHA384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#sha384"<br/> |
| Всзури \_ xmlns \_ дигсиг \_ SHA512<br/> | "https://www.w3.org/2001/04/xmlenc\#sha512"<br/>       |



 

Методы подписи



| Константа                                        | Значение URI                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| Всзури \_ xmlns \_ дигсиг \_ RSA \_ SHA1<br/>     | "https://www.w3.org/2000/09/xmldsig\#rsa-sha1"<br/>          |
| \_ \_ \_ SHA1 дигсиг DSA \_ всзури<br/>     | "https://www.w3.org/2000/09/xmldsig\#dsa-sha1"<br/>          |
| Всзури \_ xmlns \_ дигсиг \_ RSA \_ SHA256<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"<br/>   |
| Всзури \_ xmlns \_ дигсиг \_ RSA \_ SHA384<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"<br/>   |
| Всзури \_ xmlns \_ дигсиг \_ RSA \_ SHA512<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"<br/>   |
| Всзури \_ xmlns \_ дигсиг \_ ECDSA \_ SHA1<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"<br/>   |
| Всзури \_ xmlns \_ дигсиг \_ ECDSA \_ SHA256<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"<br/> |
| Всзури \_ xmlns \_ дигсиг \_ ECDSA \_ SHA384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"<br/> |
| Всзури \_ xmlns \_ дигсиг \_ ECDSA \_ SHA512<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"<br/> |
| Всзури \_ xmlns \_ дигсиг \_ HMAC \_ SHA1<br/>    | "https://www.w3.org/2000/09/xmldsig\#hmac-sha1"<br/>         |
| Всзури \_ xmlns \_ дигсиг \_ HMAC \_ SHA256<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"<br/>  |
| Всзури \_ xmlns \_ дигсиг \_ HMAC \_ SHA384<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"<br/>  |
| Всзури \_ xmlns \_ дигсиг \_ HMAC \_ SHA512<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"<br/>  |



 

 

 
