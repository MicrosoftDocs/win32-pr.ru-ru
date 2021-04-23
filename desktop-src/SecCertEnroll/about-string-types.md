---
description: Одним из наиболее распространенных способов использования строк в инфраструктуре открытых ключей является создание различающегося имени X. 500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Строковые типы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1173de3b2c4c5fd64181cd19c69cfbcecb1d584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264479"
---
# <a name="string-types"></a><span data-ttu-id="a9adc-103">Строковые типы</span><span class="sxs-lookup"><span data-stu-id="a9adc-103">String Types</span></span>

<span data-ttu-id="a9adc-104">Одним из наиболее распространенных способов использования строк в инфраструктуре открытых ключей является создание различающегося имени X. 500.</span><span class="sxs-lookup"><span data-stu-id="a9adc-104">One of the most common uses of strings in a public key infrastructure (PKI) is to create an X.500 Distinguished Name.</span></span> <span data-ttu-id="a9adc-105">Например, имя субъекта запроса на сертификат создается путем объединения последовательности относительных различающихся имен, как показано в следующем примере синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="a9adc-105">For example, the subject name of a certificate request is created by combining a sequence of relative distinguished names as shown in the following syntax example.</span></span>

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

<span data-ttu-id="a9adc-106">API регистрации сертификатов поддерживает следующие типы строк ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="a9adc-106">The Certificate Enrollment API supports the following ASN.1 string types.</span></span>

## <a name="bmpstring"></a><span data-ttu-id="a9adc-107">бмпстринг</span><span class="sxs-lookup"><span data-stu-id="a9adc-107">BMPString</span></span>

<span data-ttu-id="a9adc-108">Тег Encoding: 0x1E</span><span class="sxs-lookup"><span data-stu-id="a9adc-108">Encoding tag: 0x1E</span></span>

<span data-ttu-id="a9adc-109">Имя Certreq.exe: строка в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="a9adc-109">Certreq.exe name: UNICODE\_STRING</span></span>

<span data-ttu-id="a9adc-110">Базовая многоязыковая плоскость (BMP) — это кодировка символов, охватывающая первую плоскость универсального набора символов (UCS).</span><span class="sxs-lookup"><span data-stu-id="a9adc-110">The Basic Multilingual Plane (BMP) is a character encoding that encompasses the first plane of the Universal Character Set (UCS).</span></span> <span data-ttu-id="a9adc-111">Есть Севентин плоскости с номерами от 0 до 16.</span><span class="sxs-lookup"><span data-stu-id="a9adc-111">There are seventeen planes numbered 0 to 16.</span></span> <span data-ttu-id="a9adc-112">BMP занимает плоскость 0 и включает 65 536 кодовых позиций из Символ 0x0000 в 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="a9adc-112">BMP occupies plane 0 and includes 65,536 code points from 0x0000 to 0xFFFF.</span></span> <span data-ttu-id="a9adc-113">Это раздел таблицы символов Юникода, где до сих пор были выполнены большинство назначений символов.</span><span class="sxs-lookup"><span data-stu-id="a9adc-113">This is the section of the Unicode character map where most of the characters assignments have so far been made.</span></span> <span data-ttu-id="a9adc-114">Он включает Латинский, средний Восточной, Восточно-Азиатский, Африканский и другой Языки.</span><span class="sxs-lookup"><span data-stu-id="a9adc-114">It includes Latin, Middle Eastern, Asian, African, and other languages.</span></span>

## <a name="ia5string"></a><span data-ttu-id="a9adc-115">IA5String</span><span class="sxs-lookup"><span data-stu-id="a9adc-115">IA5String</span></span>

<span data-ttu-id="a9adc-116">Тег Encoding: 0x16</span><span class="sxs-lookup"><span data-stu-id="a9adc-116">Encoding tag: 0x16</span></span>

<span data-ttu-id="a9adc-117">Имя Certreq.exe: \_ строка IA5</span><span class="sxs-lookup"><span data-stu-id="a9adc-117">Certreq.exe name: IA5\_STRING</span></span>

<span data-ttu-id="a9adc-118">Международный алфавит номер 5 (IA5) обычно эквивалентен алфавиту ASCII, но разные версии могут включать диакритические знаки или другие символы, относящиеся к региональному языку.</span><span class="sxs-lookup"><span data-stu-id="a9adc-118">The International Alphabet number 5 (IA5) is generally equivalent to the ASCII alphabet, but different versions can include accents or other characters specific to a regional language.</span></span> <span data-ttu-id="a9adc-119">В следующем примере показан тип **IA5String** , используемый в определении ASN. 1 расширения сертификата **алтернативенамес** .</span><span class="sxs-lookup"><span data-stu-id="a9adc-119">The following example shows the **IA5String** type used in the ASN.1 definition of the **AlternativeNames** certificate extension.</span></span>

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

## <a name="printablestring"></a><span data-ttu-id="a9adc-120">принтаблестринг</span><span class="sxs-lookup"><span data-stu-id="a9adc-120">PrintableString</span></span>

<span data-ttu-id="a9adc-121">Тег Encoding: 0x13</span><span class="sxs-lookup"><span data-stu-id="a9adc-121">Encoding tag: 0x13</span></span>

<span data-ttu-id="a9adc-122">Имя Certreq.exe: строка с возможностью печати \_</span><span class="sxs-lookup"><span data-stu-id="a9adc-122">Certreq.exe name: PRINTABLE\_STRING</span></span>

<span data-ttu-id="a9adc-123">Тип данных **принтаблестринг** изначально предназначался для представления ограниченных наборов символов, доступных для терминалов ввода мэйнфреймов, но он по-прежнему часто используется.</span><span class="sxs-lookup"><span data-stu-id="a9adc-123">The **PrintableString** data type was originally intended to represent the limited character sets available to mainframe input terminals, but it is still commonly used.</span></span> <span data-ttu-id="a9adc-124">Он содержит следующие символы:</span><span class="sxs-lookup"><span data-stu-id="a9adc-124">It contains the following characters:</span></span>

-   <span data-ttu-id="a9adc-125">A – Z</span><span class="sxs-lookup"><span data-stu-id="a9adc-125">A-Z</span></span>
-   <span data-ttu-id="a9adc-126">a – z</span><span class="sxs-lookup"><span data-stu-id="a9adc-126">a-z</span></span>
-   <span data-ttu-id="a9adc-127">0-9</span><span class="sxs-lookup"><span data-stu-id="a9adc-127">0-9</span></span>
-   <span data-ttu-id="a9adc-128">' ( ) + , - .</span><span class="sxs-lookup"><span data-stu-id="a9adc-128">' ( ) + , - .</span></span> <span data-ttu-id="a9adc-129">/ : = ?</span><span class="sxs-lookup"><span data-stu-id="a9adc-129">/ : = ?</span></span> <span data-ttu-id="a9adc-130">\[space\]</span><span class="sxs-lookup"><span data-stu-id="a9adc-130">\[space\]</span></span>

## <a name="teletexstring"></a><span data-ttu-id="a9adc-131">телетексстринг</span><span class="sxs-lookup"><span data-stu-id="a9adc-131">TeletexString</span></span>

<span data-ttu-id="a9adc-132">Тег Encoding: 0x14</span><span class="sxs-lookup"><span data-stu-id="a9adc-132">Encoding tag: 0x14</span></span>

<span data-ttu-id="a9adc-133">**Телетексстринг** и связанные типы данных **T61String** кодируются на 8 бит (или 16 бит для составных символов).</span><span class="sxs-lookup"><span data-stu-id="a9adc-133">The **TeletexString** and the related **T61String** data types are encoded on 8 bits (or 16 bits for composite characters).</span></span> <span data-ttu-id="a9adc-134">У них есть номер тега 0x14.</span><span class="sxs-lookup"><span data-stu-id="a9adc-134">They both have a tag number of 0x14.</span></span> <span data-ttu-id="a9adc-135">Они не используются широко.</span><span class="sxs-lookup"><span data-stu-id="a9adc-135">They are not extensively used.</span></span>

## <a name="utf8string"></a><span data-ttu-id="a9adc-136">Образец UTF8String</span><span class="sxs-lookup"><span data-stu-id="a9adc-136">UTF8String</span></span>

<span data-ttu-id="a9adc-137">Тег Encoding: 0x0C</span><span class="sxs-lookup"><span data-stu-id="a9adc-137">Encoding tag: 0x0C</span></span>

<span data-ttu-id="a9adc-138">Имя Certreq.exe: \_ строка UTF8</span><span class="sxs-lookup"><span data-stu-id="a9adc-138">Certreq.exe name: UTF8\_STRING</span></span>

<span data-ttu-id="a9adc-139">8-разрядный формат преобразования UCS/Юникода (UTF-8) представляет собой кодировку символов переменной длины, которая может представлять любой универсальный символ в виде символа Юникода, одновременно позволяя исходным точкам кода оставаться единообразными в кодировке ASCII.</span><span class="sxs-lookup"><span data-stu-id="a9adc-139">The 8-bit UCS/Unicode Transformation Format (UTF-8) is a variable-length character encoding that can represent any universal character as a Unicode character while allowing initial code points to remain consistent with ASCII.</span></span> <span data-ttu-id="a9adc-140">UTF-8 использует от одного до четырех байтов.</span><span class="sxs-lookup"><span data-stu-id="a9adc-140">UTF-8 uses one to four bytes.</span></span> <span data-ttu-id="a9adc-141">Номер тега — 0x0C.</span><span class="sxs-lookup"><span data-stu-id="a9adc-141">The tag number is 0x0C.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9adc-142">См. также</span><span class="sxs-lookup"><span data-stu-id="a9adc-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9adc-143">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="a9adc-143">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="a9adc-144">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="a9adc-144">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="a9adc-145">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="a9adc-145">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



