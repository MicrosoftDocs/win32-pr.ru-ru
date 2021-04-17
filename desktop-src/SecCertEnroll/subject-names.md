---
description: Поле subject запроса на сертификат PKCS \# 10 содержит различающееся имя сущности, запрашивающей сертификат.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Имена субъектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 226c294e75477a3960cd0ad824a98b3556c34322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663626"
---
# <a name="subject-names"></a>Имена субъектов

Поле **subject** запроса на сертификат PKCS \# 10 содержит различающееся имя сущности, запрашивающей сертификат.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

Различающееся имя состоит из последовательности относительных различающихся имен (Рднс). Каждый RDN состоит из набора атрибутов, и каждый атрибут состоит из идентификатора объекта и значения. Тип данных значения определяется структурой **директористринг** .

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

Дополнительные сведения см. в следующих разделах:

-   [Создание имени субъекта](creating-a-subject-name.md)
-   [Кодирование имени субъекта](encoding-a-subject-name.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Запросы](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
