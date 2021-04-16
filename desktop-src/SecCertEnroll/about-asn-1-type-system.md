---
description: Понятие типа данных является фундаментальным для нотации абстрактного синтаксиса — 1 (ASN. 1) Standard.
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: Система типов ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbf60bf61e32c5fca882f2e40c946c043ef93e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664648"
---
# <a name="asn1-type-system"></a>Система типов ASN. 1

Понятие типа данных является фундаментальным для нотации абстрактного синтаксиса — 1 (ASN. 1) Standard. Каждое поле структуры запроса на сертификат связано с типом. Рассмотрим, например, \# синтаксис сертификата PKCS 10 ASN. 1, как показано в следующем примере.

``` syntax
--------------------------------------------------------------------
-- PKCS #10 Certificate request.
--------------------------------------------------------------------
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

--------------------------------------------------------------------
-- Version number.
--------------------------------------------------------------------
CertificationRequestInfoVersion ::= INTEGER

--------------------------------------------------------------------
-- Subject distinguished name (DN).
--------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}

--------------------------------------------------------------------
-- Public key information.
--------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
   algorithm           AlgorithmIdentifier,
   subjectPublicKey    BITSTRING
}

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
} 

--------------------------------------------------------------------
-- Attributes.
--------------------------------------------------------------------
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   values             AttributeSetValue
}

AttributeSetValue ::= SET OF ANY
```

Высокоуровневая структура запросов, **CertificationRequestInfo**, представляет собой тип, который состоит из последовательности других типов. Если тип или содержит только базовые типы, строковые типы или **ANY**, он не может быть разбит дальше. Например, поле **Version** является типом **цертификатионрекуестинфоверсион** , который, в свою очередь, является базовым **типом ASN** . 1, не состоящим из других типов.

Система типов позволяет визуально представить синтаксис запроса, понятный разработчикам, и обеспечивает единообразное кодирование запроса для передачи по сети. Дополнительные сведения о кодировке см. в разделе [distinguished Encoding Rules](distinguished-encoding-rules.md). Дополнительные сведения о типах ASN. 1 см. в следующих разделах.

[Базовые типы](about-basic-types.md)

Описывает следующие типы данных:

* **БИТОВАЯ СТРОКА**
* **BOOLEAN**
* **INTEGER**
* **NULL**
* **ИДЕНТИФИКАТОР ОБЪЕКТА**
* **СТРОКА ОКТЕТА**

[Строковые типы](about-string-types.md)

Описывает следующие типы строк:

* **бмпстринг**
* **IA5String**
* **принтаблестринг**
* **телетексстринг**
* **Образец UTF8String**

[Сконструированные типы](about-constructed-types.md)

Описывает типы данных ASN. 1, которые могут содержать базовые типы, строковые типы или другие сконструированные типы.




 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Кодирование запроса сертификата](about-certificate-request-encoding.md)
</dt> <dt>

[Кодировка DER для типов ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Общие сведения о синтаксисе и кодировке ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



