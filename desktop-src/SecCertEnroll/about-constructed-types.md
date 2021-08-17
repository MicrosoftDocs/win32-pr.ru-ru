---
description: Сконструированная абстрактная нотация синтаксиса One (ASN. 1) состоит из базовых типов, строковых типов или других сконструированных типов. Например, расширение сертификата X. 509 состоит из трех основных типов ASN. 1, как показано в следующем примере.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Сконструированные типы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ed62c4a59bfc0944ad5e31673ab0ea9031c0175014c8fc1c6b6f2cc071b153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904493"
---
# <a name="constructed-types"></a>Сконструированные типы

Сконструированная [*абстрактная нотация синтаксиса One*](/windows/desktop/SecGloss/a-gly) (ASN. 1) состоит из базовых типов, строковых типов или других сконструированных типов. Например, расширение сертификата X. 509 состоит из трех основных типов ASN. 1, как показано в следующем примере.

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

Расширение состоит из [*идентификатора объекта*](/windows/desktop/SecGloss/o-gly) (OID), логического значения, определяющего, является ли расширение критическим, и массива байтов, содержащего это значение. API регистрации сертификатов поддерживает следующие сконструированные типы ASN. 1.

## <a name="sequence-and-sequence-of"></a>ПОСЛЕДОВАТЕЛЬНОСТЬ и последовательность

Тег Encoding: 0x30

Содержит упорядоченную последовательность полей одного или нескольких типов. Поля могут быть помечены как **необязательные** или **по умолчанию**. Кроме того, чтобы избежать неоднозначности при декодировании, последовательные необязательные поля должны отличаться друг от друга за счет использования уникального идентификатора (целое число в квадратных скобках, например \[ 1 \] ) и из следующего обязательного поля, как показано в следующем примере.

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

Разница между **последовательностью** и **последовательностью** состоит в том, что элементы **последовательности** конструкций должны иметь один и тот же тип. См. следующий пример. При кодировании обе конструкции имеют одинаковое значение тега (0x30).

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

Другой способ узнать разницу между **последовательностью** и **последовательностью** — сравнить их с их аналогами в языке программирования C. Это значит, что **последовательность** примерно эквивалентна структуре и **последовательности** , что примерно эквивалентно массиву.

## <a name="set-and-set-of"></a>НАБОР и набор

Тег Encoding: 0x31

Содержит неупорядоченную последовательность полей одного или нескольких типов. Это отличается от **последовательности** , содержащей упорядоченный список. Задание неупорядоченного списка позволяет приложению предоставлять поля структуры кодировщику в наиболее подходящем порядке. Как и в случае с **Sequence**, поля конструкции **набора** могут быть помечены **дополнительным** или **по умолчанию**, а уникальные идентификаторы должны использоваться для устранения неоднозначности процесса декодирования. Различие между **набором** и набором состоит в том, что элементы **набора** конструкций должны иметь **один и тот** же тип.

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a>УСМОТРЕНИ

Тег Encoding: неприменимо

Определяет выбор между альтернативами. Каждый вариант должен быть однозначно идентифицирован целым числом в квадратных скобках, чтобы избежать неоднозначности при декодировании. При кодировании конструкция **выбора** будет иметь значение тега Encoding выбранной альтернативы.

``` syntax
AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SeqOfAny,
   directoryName           [4] EXPLICIT Name,
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Система типов ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Кодировка DER для типов ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 
