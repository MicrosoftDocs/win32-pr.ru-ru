---
description: Сертификат X. 509 версии 1 содержит следующие поля. Поля версии 2 рассматриваются в полях версии 2. Поля версии 3 рассматриваются в разделе расширения версии 3.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Основные поля
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad24afa21787227b3fe47ab187a97c7886c9c9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909655"
---
# <a name="basic-fields"></a><span data-ttu-id="94838-105">Основные поля</span><span class="sxs-lookup"><span data-stu-id="94838-105">Basic Fields</span></span>

<span data-ttu-id="94838-106">Сертификат X. 509 версии 1 содержит следующие поля.</span><span class="sxs-lookup"><span data-stu-id="94838-106">An X.509 version 1 certificate contains the following fields.</span></span> <span data-ttu-id="94838-107">Поля версии 2 рассматриваются в [полях версии 2](about-version-2-fields.md).</span><span class="sxs-lookup"><span data-stu-id="94838-107">Version 2 fields are discussed in [Version 2 Fields](about-version-2-fields.md).</span></span> <span data-ttu-id="94838-108">Поля версии 3 рассматриваются в разделе [расширения версии 3](about-version-3-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="94838-108">Version 3 fields are discussed in [Version 3 Extensions](about-version-3-extensions.md).</span></span>

## <a name="version"></a><span data-ttu-id="94838-109">Версия</span><span class="sxs-lookup"><span data-stu-id="94838-109">Version</span></span>

<span data-ttu-id="94838-110">Указывает номер версии закодированного сертификата.</span><span class="sxs-lookup"><span data-stu-id="94838-110">Specifies the version number of the encoded certificate.</span></span> <span data-ttu-id="94838-111">В настоящее время возможные значения этого поля: 0, 1 или 2, но это может быть расширено в будущем.</span><span class="sxs-lookup"><span data-stu-id="94838-111">Currently, the possible values of this field are 0, 1, or 2, but this may be expanded in the future.</span></span>

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a><span data-ttu-id="94838-112">Серийный номер</span><span class="sxs-lookup"><span data-stu-id="94838-112">Serial Number</span></span>

<span data-ttu-id="94838-113">Содержит положительное уникальное целое число, присвоенное сертификату центром сертификации (ЦС).</span><span class="sxs-lookup"><span data-stu-id="94838-113">Contains a positive, unique integer assigned by the certification authority (CA) to the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a><span data-ttu-id="94838-114">Алгоритм подписи</span><span class="sxs-lookup"><span data-stu-id="94838-114">Signature Algorithm</span></span>

<span data-ttu-id="94838-115">Содержит [*идентификатор объекта*](/windows/desktop/SecGloss/o-gly) (OID), указывающий алгоритм, используемый ЦС для подписи сертификата.</span><span class="sxs-lookup"><span data-stu-id="94838-115">Contains an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) that specifies the algorithm used by the CA to sign the certificate.</span></span> <span data-ttu-id="94838-116">Например, 1.2.840.113549.1.1.5 указывает на использование хэш-алгоритма SHA-1 вместе с алгоритмом шифрования RSA, разработанного RSA Laboratories.</span><span class="sxs-lookup"><span data-stu-id="94838-116">For example, 1.2.840.113549.1.1.5 specifies a SHA-1 hashing algorithm combined with the RSA encryption algorithm from RSA Laboratories.</span></span>

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

## <a name="issuer"></a><span data-ttu-id="94838-117">Издатель</span><span class="sxs-lookup"><span data-stu-id="94838-117">Issuer</span></span>

<span data-ttu-id="94838-118">Содержит различающееся имя [*X. 500*](/windows/desktop/SecGloss/x-gly) ЦС, который создал и подписал сертификат.</span><span class="sxs-lookup"><span data-stu-id="94838-118">Contains the [*X.500*](/windows/desktop/SecGloss/x-gly) distinguished name (DN) of the CA that created and signed the certificate.</span></span>

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

## <a name="validity"></a><span data-ttu-id="94838-119">Срок действия</span><span class="sxs-lookup"><span data-stu-id="94838-119">Validity</span></span>

<span data-ttu-id="94838-120">Указывает промежуток времени, в течение которого действует сертификат.</span><span class="sxs-lookup"><span data-stu-id="94838-120">Specifies the time interval during which the certificate is valid.</span></span> <span data-ttu-id="94838-121">Даты до конца 2049 используют формат времени в формате UTC (время по Гринвичу) (*ииммддххммссз*).</span><span class="sxs-lookup"><span data-stu-id="94838-121">Dates through the end of 2049 use the Coordinated Universal Time (Greenwich Mean Time) format (*yymmddhhmmssz*).</span></span> <span data-ttu-id="94838-122">Даты, начинающиеся с 1 января 2050 г., используют обобщенный формат времени (*ииииммддххммссз*).</span><span class="sxs-lookup"><span data-stu-id="94838-122">Dates beginning with January 1st, 2050 use the generalized time format (*yyyymmddhhmmssz*).</span></span>

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

## <a name="subject"></a><span data-ttu-id="94838-123">Субъект</span><span class="sxs-lookup"><span data-stu-id="94838-123">Subject</span></span>

<span data-ttu-id="94838-124">Содержит различающееся имя X.500 объекта, связанного с открытым ключом, содержащимся в сертификате.</span><span class="sxs-lookup"><span data-stu-id="94838-124">Contains an X.500 distinguished name of the entity associated with the public key contained in the certificate.</span></span>

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

## <a name="public-key"></a><span data-ttu-id="94838-125">Открытый ключ</span><span class="sxs-lookup"><span data-stu-id="94838-125">Public Key</span></span>

<span data-ttu-id="94838-126">Содержит открытый ключ и данные связанного алгоритма.</span><span class="sxs-lookup"><span data-stu-id="94838-126">Contains the public key and associated algorithm information.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="94838-127">См. также</span><span class="sxs-lookup"><span data-stu-id="94838-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94838-128">Поля версии 2</span><span class="sxs-lookup"><span data-stu-id="94838-128">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="94838-129">Расширения версии 3</span><span class="sxs-lookup"><span data-stu-id="94838-129">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="94838-130">Сертификаты открытого ключа X. 509</span><span class="sxs-lookup"><span data-stu-id="94838-130">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 
