---
description: Одним из наиболее распространенных способов использования строк в инфраструктуре открытых ключей является создание различающегося имени X. 500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Строковые типы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9e190e10bc86bd68a344f5aa279b4812bc04437418578320c36e0e1791dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903693"
---
# <a name="string-types"></a>Строковые типы

Одним из наиболее распространенных способов использования строк в инфраструктуре открытых ключей является создание различающегося имени X. 500. Например, имя субъекта запроса на сертификат создается путем объединения последовательности относительных различающихся имен, как показано в следующем примере синтаксиса.

``` syntax
---------------------------------------------------------------------
-- Breakdown of a subject name in a certificate request.
---------------------------------------------------------------------

CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
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

API регистрации сертификатов поддерживает следующие типы строк ASN. 1.

## <a name="bmpstring"></a>бмпстринг

Тег Encoding: 0x1E

Имя Certreq.exe: строка в Юникоде \_

Базовая многоязыковая плоскость (BMP) — это кодировка символов, охватывающая первую плоскость универсального набора символов (UCS). Есть Севентин плоскости с номерами от 0 до 16. BMP занимает плоскость 0 и включает 65 536 кодовых позиций из Символ 0x0000 в 0xFFFF. Это раздел таблицы символов Юникода, где до сих пор были выполнены большинство назначений символов. Он включает Латинский, средний Восточной, Восточно-Азиатский, Африканский и другой Языки.

## <a name="ia5string"></a>IA5String

Тег Encoding: 0x16

Имя Certreq.exe: \_ строка IA5

Международный алфавит номер 5 (IA5) обычно эквивалентен алфавиту ASCII, но разные версии могут включать диакритические знаки или другие символы, относящиеся к региональному языку. В следующем примере показан тип **IA5String** , используемый в определении ASN. 1 расширения сертификата **алтернативенамес** .

``` syntax
---------------------------------------------------------------------
-- AlternativeNames extension
---------------------------------------------------------------------

AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SEQUENCE OF ANY, 
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}

OtherName ::= SEQUENCE 
{
   type                    OBJECT IDENTIFIER,
   value                   [0] EXPLICIT ANY 
}
```

## <a name="printablestring"></a>принтаблестринг

Тег Encoding: 0x13

Имя Certreq.exe: строка с возможностью печати \_

Тип данных **принтаблестринг** изначально предназначался для представления ограниченных наборов символов, доступных для терминалов ввода мэйнфреймов, но он по-прежнему часто используется. Он содержит следующие символы:

-   A – Z
-   a – z
-   0-9
-   ' ( ) + , - . / : = ? \[space\]

## <a name="teletexstring"></a>телетексстринг

Тег Encoding: 0x14

**Телетексстринг** и связанные типы данных **T61String** кодируются на 8 бит (или 16 бит для составных символов). У них есть номер тега 0x14. Они не используются широко.

## <a name="utf8string"></a>Образец UTF8String

Тег Encoding: 0x0C

Имя Certreq.exe: \_ строка UTF8

8-разрядный формат преобразования UCS/Юникода (UTF-8) представляет собой кодировку символов переменной длины, которая может представлять любой универсальный символ в виде символа Юникода, одновременно позволяя исходным точкам кода оставаться единообразными в кодировке ASCII. UTF-8 использует от одного до четырех байтов. Номер тега — 0x0C.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Система типов ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Кодировка DER для типов ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



