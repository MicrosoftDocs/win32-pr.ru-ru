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
# <a name="asn1-type-system"></a><span data-ttu-id="2c85c-103">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2c85c-103">ASN.1 Type System</span></span>

<span data-ttu-id="2c85c-104">Понятие типа данных является фундаментальным для нотации абстрактного синтаксиса — 1 (ASN. 1) Standard.</span><span class="sxs-lookup"><span data-stu-id="2c85c-104">The concept of a data type is fundamental to the Abstract Syntax Notation One (ASN.1) standard.</span></span> <span data-ttu-id="2c85c-105">Каждое поле структуры запроса на сертификат связано с типом.</span><span class="sxs-lookup"><span data-stu-id="2c85c-105">Every field of a certificate request structure is associated with a type.</span></span> <span data-ttu-id="2c85c-106">Рассмотрим, например, \# синтаксис сертификата PKCS 10 ASN. 1, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="2c85c-106">Consider, for example, the PKCS \#10 ASN.1 certificate syntax shown in the following example.</span></span>

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

<span data-ttu-id="2c85c-107">Высокоуровневая структура запросов, **CertificationRequestInfo**, представляет собой тип, который состоит из последовательности других типов.</span><span class="sxs-lookup"><span data-stu-id="2c85c-107">The high-level request structure, **CertificationRequestInfo**, is a type that is made up from a sequence of other types.</span></span> <span data-ttu-id="2c85c-108">Если тип или содержит только базовые типы, строковые типы или **ANY**, он не может быть разбит дальше.</span><span class="sxs-lookup"><span data-stu-id="2c85c-108">When a type is or contains only basic types, string types, or **ANY**, it cannot be broken down further.</span></span> <span data-ttu-id="2c85c-109">Например, поле **Version** является типом **цертификатионрекуестинфоверсион** , который, в свою очередь, является базовым **типом ASN** . 1, не состоящим из других типов.</span><span class="sxs-lookup"><span data-stu-id="2c85c-109">For example, the **version** field is a **CertificationRequestInfoVersion** type which is, in turn, an **INTEGER** type, a basic ASN.1 type that is not composed from other types.</span></span>

<span data-ttu-id="2c85c-110">Система типов позволяет визуально представить синтаксис запроса, понятный разработчикам, и обеспечивает единообразное кодирование запроса для передачи по сети.</span><span class="sxs-lookup"><span data-stu-id="2c85c-110">A type system enables the syntax of a request to be presented visually in a manner readily understood by developers, and it enables the request to be consistently encoded for transmission across a network.</span></span> <span data-ttu-id="2c85c-111">Дополнительные сведения о кодировке см. в разделе [distinguished Encoding Rules](distinguished-encoding-rules.md).</span><span class="sxs-lookup"><span data-stu-id="2c85c-111">For more information about encoding, see [Distinguished Encoding Rules](distinguished-encoding-rules.md).</span></span> <span data-ttu-id="2c85c-112">Дополнительные сведения о типах ASN. 1 см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="2c85c-112">For more information about ASN.1 types, see the following topics.</span></span>

[<span data-ttu-id="2c85c-113">Базовые типы</span><span class="sxs-lookup"><span data-stu-id="2c85c-113">Basic Types</span></span>](about-basic-types.md)

<span data-ttu-id="2c85c-114">Описывает следующие типы данных:</span><span class="sxs-lookup"><span data-stu-id="2c85c-114">Discusses the following data types:</span></span>

* <span data-ttu-id="2c85c-115">**БИТОВАЯ СТРОКА**</span><span class="sxs-lookup"><span data-stu-id="2c85c-115">**BIT STRING**</span></span>
* <span data-ttu-id="2c85c-116">**BOOLEAN**</span><span class="sxs-lookup"><span data-stu-id="2c85c-116">**BOOLEAN**</span></span>
* <span data-ttu-id="2c85c-117">**INTEGER**</span><span class="sxs-lookup"><span data-stu-id="2c85c-117">**INTEGER**</span></span>
* <span data-ttu-id="2c85c-118">**NULL**</span><span class="sxs-lookup"><span data-stu-id="2c85c-118">**NULL**</span></span>
* <span data-ttu-id="2c85c-119">**ИДЕНТИФИКАТОР ОБЪЕКТА**</span><span class="sxs-lookup"><span data-stu-id="2c85c-119">**OBJECT IDENTIFIER**</span></span>
* <span data-ttu-id="2c85c-120">**СТРОКА ОКТЕТА**</span><span class="sxs-lookup"><span data-stu-id="2c85c-120">**OCTET STRING**</span></span>

[<span data-ttu-id="2c85c-121">Строковые типы</span><span class="sxs-lookup"><span data-stu-id="2c85c-121">String Types</span></span>](about-string-types.md)

<span data-ttu-id="2c85c-122">Описывает следующие типы строк:</span><span class="sxs-lookup"><span data-stu-id="2c85c-122">Discusses the following string types:</span></span>

* <span data-ttu-id="2c85c-123">**бмпстринг**</span><span class="sxs-lookup"><span data-stu-id="2c85c-123">**BMPString**</span></span>
* <span data-ttu-id="2c85c-124">**IA5String**</span><span class="sxs-lookup"><span data-stu-id="2c85c-124">**IA5String**</span></span>
* <span data-ttu-id="2c85c-125">**принтаблестринг**</span><span class="sxs-lookup"><span data-stu-id="2c85c-125">**PrintableString**</span></span>
* <span data-ttu-id="2c85c-126">**телетексстринг**</span><span class="sxs-lookup"><span data-stu-id="2c85c-126">**TeletexString**</span></span>
* <span data-ttu-id="2c85c-127">**Образец UTF8String**</span><span class="sxs-lookup"><span data-stu-id="2c85c-127">**UTF8String**</span></span>

[<span data-ttu-id="2c85c-128">Сконструированные типы</span><span class="sxs-lookup"><span data-stu-id="2c85c-128">Constructed Types</span></span>](about-constructed-types.md)

<span data-ttu-id="2c85c-129">Описывает типы данных ASN. 1, которые могут содержать базовые типы, строковые типы или другие сконструированные типы.</span><span class="sxs-lookup"><span data-stu-id="2c85c-129">Discusses ASN.1 data types that can contain basic types, string types, or other constructed types.</span></span>




 

## <a name="related-topics"></a><span data-ttu-id="2c85c-130">См. также</span><span class="sxs-lookup"><span data-stu-id="2c85c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c85c-131">Кодирование запроса сертификата</span><span class="sxs-lookup"><span data-stu-id="2c85c-131">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="2c85c-132">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2c85c-132">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="2c85c-133">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="2c85c-133">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="2c85c-134">Общие сведения о синтаксисе и кодировке ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2c85c-134">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



