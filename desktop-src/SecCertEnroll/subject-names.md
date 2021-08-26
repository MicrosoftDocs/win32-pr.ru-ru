---
description: Поле subject запроса на сертификат PKCS \# 10 содержит различающееся имя сущности, запрашивающей сертификат.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Имена субъектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be70af23c524e71c1a9b22f43e391e4f5c8302fba70f24fba1f8268ebfda6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101104"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запросы](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
