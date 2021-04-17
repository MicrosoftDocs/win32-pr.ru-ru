---
description: Сконструированная абстрактная нотация синтаксиса One (ASN. 1) состоит из базовых типов, строковых типов или других сконструированных типов. Например, расширение сертификата X. 509 состоит из трех основных типов ASN. 1, как показано в следующем примере.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Сконструированные типы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a515e6e03ebf3c95ff1cabc1bf7f12eb423df27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662330"
---
# <a name="constructed-types"></a><span data-ttu-id="3d68a-104">Сконструированные типы</span><span class="sxs-lookup"><span data-stu-id="3d68a-104">Constructed Types</span></span>

<span data-ttu-id="3d68a-105">Сконструированная [*абстрактная нотация синтаксиса One*](/windows/desktop/SecGloss/a-gly) (ASN. 1) состоит из базовых типов, строковых типов или других сконструированных типов.</span><span class="sxs-lookup"><span data-stu-id="3d68a-105">A constructed [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) type is made up from basic types, string types, or other constructed types.</span></span> <span data-ttu-id="3d68a-106">Например, расширение сертификата X. 509 состоит из трех основных типов ASN. 1, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="3d68a-106">For example, an X.509 certificate extension is composed from three basic ASN.1 types as shown by the following example.</span></span>

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

<span data-ttu-id="3d68a-107">Расширение состоит из [*идентификатора объекта*](/windows/desktop/SecGloss/o-gly) (OID), логического значения, определяющего, является ли расширение критическим, и массива байтов, содержащего это значение.</span><span class="sxs-lookup"><span data-stu-id="3d68a-107">An extension consists of an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the value.</span></span> <span data-ttu-id="3d68a-108">API регистрации сертификатов поддерживает следующие сконструированные типы ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="3d68a-108">The Certificate Enrollment API supports the following constructed ASN.1 types.</span></span>

## <a name="sequence-and-sequence-of"></a><span data-ttu-id="3d68a-109">ПОСЛЕДОВАТЕЛЬНОСТЬ и последовательность</span><span class="sxs-lookup"><span data-stu-id="3d68a-109">SEQUENCE and SEQUENCE OF</span></span>

<span data-ttu-id="3d68a-110">Тег Encoding: 0x30</span><span class="sxs-lookup"><span data-stu-id="3d68a-110">Encoding tag: 0x30</span></span>

<span data-ttu-id="3d68a-111">Содержит упорядоченную последовательность полей одного или нескольких типов.</span><span class="sxs-lookup"><span data-stu-id="3d68a-111">Contains an ordered series of fields of one or more types.</span></span> <span data-ttu-id="3d68a-112">Поля могут быть помечены как **необязательные** или **по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="3d68a-112">Fields can be marked **OPTIONAL** or **DEFAULT**.</span></span> <span data-ttu-id="3d68a-113">Кроме того, чтобы избежать неоднозначности при декодировании, последовательные необязательные поля должны отличаться друг от друга за счет использования уникального идентификатора (целое число в квадратных скобках, например \[ 1 \] ) и из следующего обязательного поля, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="3d68a-113">Also, to avoid ambiguity when decoding, successive optional fields should differ from one another by use of a unique identifier (a bracketed integer such as \[1\]) and from a following required field as shown by the following example.</span></span>

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

<span data-ttu-id="3d68a-114">Разница между **последовательностью** и **последовательностью** состоит в том, что элементы **последовательности** конструкций должны иметь один и тот же тип.</span><span class="sxs-lookup"><span data-stu-id="3d68a-114">The difference between **SEQUENCE** and **SEQUENCE OF** is that the elements of a **SEQUENCE OF** construct must be of the same type.</span></span> <span data-ttu-id="3d68a-115">См. следующий пример.</span><span class="sxs-lookup"><span data-stu-id="3d68a-115">See the following example.</span></span> <span data-ttu-id="3d68a-116">При кодировании обе конструкции имеют одинаковое значение тега (0x30).</span><span class="sxs-lookup"><span data-stu-id="3d68a-116">Both constructs have the same tag value (0x30) when encoded.</span></span>

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

<span data-ttu-id="3d68a-117">Другой способ узнать разницу между **последовательностью** и **последовательностью** — сравнить их с их аналогами в языке программирования C.</span><span class="sxs-lookup"><span data-stu-id="3d68a-117">Another way to look at the difference between **SEQUENCE** and **SEQUENCE OF** is to compare them to their counterparts in the C programming language.</span></span> <span data-ttu-id="3d68a-118">Это значит, что **последовательность** примерно эквивалентна структуре и **последовательности** , что примерно эквивалентно массиву.</span><span class="sxs-lookup"><span data-stu-id="3d68a-118">That is, **SEQUENCE** is roughly equivalent to a structure and **SEQUENCE OF** is roughly equivalent to an array.</span></span>

## <a name="set-and-set-of"></a><span data-ttu-id="3d68a-119">НАБОР и набор</span><span class="sxs-lookup"><span data-stu-id="3d68a-119">SET and SET OF</span></span>

<span data-ttu-id="3d68a-120">Тег Encoding: 0x31</span><span class="sxs-lookup"><span data-stu-id="3d68a-120">Encoding tag: 0x31</span></span>

<span data-ttu-id="3d68a-121">Содержит неупорядоченную последовательность полей одного или нескольких типов.</span><span class="sxs-lookup"><span data-stu-id="3d68a-121">Contains an unordered series of fields of one or more types.</span></span> <span data-ttu-id="3d68a-122">Это отличается от **последовательности** , содержащей упорядоченный список.</span><span class="sxs-lookup"><span data-stu-id="3d68a-122">This differs from a **SEQUENCE** which contains an ordered list.</span></span> <span data-ttu-id="3d68a-123">Задание неупорядоченного списка позволяет приложению предоставлять поля структуры кодировщику в наиболее подходящем порядке.</span><span class="sxs-lookup"><span data-stu-id="3d68a-123">Specifying an unordered list enables an application to provide the structure fields to the encoder in the most appropriate order.</span></span> <span data-ttu-id="3d68a-124">Как и в случае с **Sequence**, поля конструкции **набора** могут быть помечены **дополнительным** или **по умолчанию**, а уникальные идентификаторы должны использоваться для устранения неоднозначности процесса декодирования.</span><span class="sxs-lookup"><span data-stu-id="3d68a-124">As with **SEQUENCE**, the fields of a **SET** construct can be marked with **OPTIONAL** or **DEFAULT**, and unique identifiers must be used to disambiguate the decoding process.</span></span> <span data-ttu-id="3d68a-125">Различие между **набором** и набором состоит в том, что элементы **набора** конструкций должны иметь **один и тот** же тип.</span><span class="sxs-lookup"><span data-stu-id="3d68a-125">The difference between **SET** and **SET OF** is that the elements of a **SET OF** construct must be of the same type.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a><span data-ttu-id="3d68a-126">УСМОТРЕНИ</span><span class="sxs-lookup"><span data-stu-id="3d68a-126">CHOICE</span></span>

<span data-ttu-id="3d68a-127">Тег Encoding: неприменимо</span><span class="sxs-lookup"><span data-stu-id="3d68a-127">Encoding tag: not applicable</span></span>

<span data-ttu-id="3d68a-128">Определяет выбор между альтернативами.</span><span class="sxs-lookup"><span data-stu-id="3d68a-128">Defines a choice between alternatives.</span></span> <span data-ttu-id="3d68a-129">Каждый вариант должен быть однозначно идентифицирован целым числом в квадратных скобках, чтобы избежать неоднозначности при декодировании.</span><span class="sxs-lookup"><span data-stu-id="3d68a-129">Each alternative must be uniquely identified by a bracketed integer to avoid ambiguity when decoding.</span></span> <span data-ttu-id="3d68a-130">При кодировании конструкция **выбора** будет иметь значение тега Encoding выбранной альтернативы.</span><span class="sxs-lookup"><span data-stu-id="3d68a-130">When encoded, the **CHOICE** construct will have the encoding tag value of the chosen alternative.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3d68a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3d68a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d68a-132">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="3d68a-132">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="3d68a-133">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="3d68a-133">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="3d68a-134">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="3d68a-134">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 
