---
description: Сертификат X. 509 версии 1 содержит следующие поля. Поля версии 2 рассматриваются в полях версии 2. Поля версии 3 рассматриваются в разделе расширения версии 3.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Основные поля
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3dae9ceaa3ddd1c4ac8a8ce86425ec32eee45e82ca8b437ed0f0c27f44817ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905089"
---
# <a name="basic-fields"></a>Основные поля

Сертификат X. 509 версии 1 содержит следующие поля. Поля версии 2 рассматриваются в [полях версии 2](about-version-2-fields.md). Поля версии 3 рассматриваются в разделе [расширения версии 3](about-version-3-extensions.md).

## <a name="version"></a>Версия

Указывает номер версии закодированного сертификата. В настоящее время возможные значения этого поля: 0, 1 или 2, но это может быть расширено в будущем.

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a>Серийный номер

Содержит положительное уникальное целое число, присвоенное сертификату центром сертификации (ЦС).

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a>Алгоритм подписи

Содержит [*идентификатор объекта*](/windows/desktop/SecGloss/o-gly) (OID), указывающий алгоритм, используемый ЦС для подписи сертификата. Например, 1.2.840.113549.1.1.5 указывает на использование хэш-алгоритма SHA-1 вместе с алгоритмом шифрования RSA, разработанного RSA Laboratories.

``` syntax
---------------------------------------------------------------------
-- Signature OID
---------------------------------------------------------------------
signature ::= AlgorithmIdentifier

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="issuer"></a>Издатель

Содержит различающееся имя [*X. 500*](/windows/desktop/SecGloss/x-gly) ЦС, который создал и подписал сертификат.

``` syntax
---------------------------------------------------------------------
-- Issuer name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="validity"></a>Срок действия

Указывает промежуток времени, в течение которого действует сертификат. Даты до конца 2049 используют формат времени в формате UTC (время по Гринвичу) (*ииммддххммссз*). Даты, начинающиеся с 1 января 2050 г., используют обобщенный формат времени (*ииииммддххммссз*).

``` syntax
---------------------------------------------------------------------
-- Validity period 
---------------------------------------------------------------------
Validity ::= SEQUENCE 
{
  notBefore           ChoiceOfTime,
  notAfter            ChoiceOfTime
}

ChoiceOfTime ::= CHOICE 
{
  utcTime                 UTCTime,
  generalTime             GeneralizedTime
}
```

## <a name="subject"></a>Тема

Содержит различающееся имя X.500 объекта, связанного с открытым ключом, содержащимся в сертификате.

``` syntax
---------------------------------------------------------------------
-- Subject name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="public-key"></a>Открытый ключ

Содержит открытый ключ и данные связанного алгоритма.

``` syntax
---------------------------------------------------------------------
--  Subject public key information
---------------------------------------------------------------------
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
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поля версии 2](about-version-2-fields.md)
</dt> <dt>

[Расширения версии 3](about-version-3-extensions.md)
</dt> <dt>

[Сертификаты открытого ключа X. 509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 
