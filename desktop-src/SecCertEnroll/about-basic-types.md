---
description: API регистрации сертификатов поддерживает следующие основные типы ASN. 1.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Базовые типы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f3ae64c058fce3466ca06e7bf205c4c4165fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647359"
---
# <a name="basic-types"></a><span data-ttu-id="73f64-103">Базовые типы</span><span class="sxs-lookup"><span data-stu-id="73f64-103">Basic Types</span></span>

<span data-ttu-id="73f64-104">API регистрации сертификатов поддерживает следующие основные типы ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="73f64-104">The Certificate Enrollment API supports the following basic ASN.1 types.</span></span>

## <a name="bit-string"></a><span data-ttu-id="73f64-105">БИТОВАЯ СТРОКА</span><span class="sxs-lookup"><span data-stu-id="73f64-105">BIT STRING</span></span>

<span data-ttu-id="73f64-106">Тег Encoding: 0x03</span><span class="sxs-lookup"><span data-stu-id="73f64-106">Encoding tag: 0x03</span></span>

<span data-ttu-id="73f64-107">Имя Certreq.exe: БИТОВАЯ \_ строка</span><span class="sxs-lookup"><span data-stu-id="73f64-107">Certreq.exe name: BIT\_STRING</span></span>

<span data-ttu-id="73f64-108">Разрядная или двоичная строка является произвольно длинным массивом битов.</span><span class="sxs-lookup"><span data-stu-id="73f64-108">A bit or binary string is an arbitrarily long array of bits.</span></span> <span data-ttu-id="73f64-109">Определенные биты можно идентифицировать с помощью целых чисел и назначенных имен, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="73f64-109">Specific bits can be identified by parenthesized integers and assigned names as in the following example.</span></span>

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

<span data-ttu-id="73f64-110">Ключи сертификатов и подписи часто представляются в виде битовых строк.</span><span class="sxs-lookup"><span data-stu-id="73f64-110">Certificate keys and signatures are often represented as bit strings.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BIT STRING
-- Tag number: 0x03
---------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
  algorithm           AlgorithmIdentifier,
  subjectPublicKey    BIT STRING
} 
```

## <a name="boolean"></a><span data-ttu-id="73f64-111">BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="73f64-111">BOOLEAN</span></span>

<span data-ttu-id="73f64-112">Тег Encoding: 0x01</span><span class="sxs-lookup"><span data-stu-id="73f64-112">Encoding tag: 0x01</span></span>

<span data-ttu-id="73f64-113">Имя Certreq.exe: логическое значение</span><span class="sxs-lookup"><span data-stu-id="73f64-113">Certreq.exe name: BOOLEAN</span></span>

<span data-ttu-id="73f64-114">Логический тип может содержать одно из двух значений: **true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="73f64-114">A Boolean type can contain one of two values, **TRUE** or **FALSE**.</span></span> <span data-ttu-id="73f64-115">В следующем примере показана структура ASN. 1 для расширения сертификата базовых ограничений.</span><span class="sxs-lookup"><span data-stu-id="73f64-115">The following example shows the ASN.1 structure for a Basic Constraints certificate extension.</span></span> <span data-ttu-id="73f64-116">В поле **cA** указывается, является ли субъект сертификата центром сертификации (CA).</span><span class="sxs-lookup"><span data-stu-id="73f64-116">The **cA** field specifies whether a certificate subject is a certification authority (CA).</span></span> <span data-ttu-id="73f64-117">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="73f64-117">The default criticality is **FALSE**.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BOOLEAN
-- Tag number: 0x01
---------------------------------------------------------------------
BasicConstraints ::= SEQUENCE 
{
  cA                  BOOLEAN DEFAULT FALSE,
  pathLenConstraint   INTEGER OPTIONAL
}
```

## <a name="integer"></a><span data-ttu-id="73f64-118">INTEGER</span><span class="sxs-lookup"><span data-stu-id="73f64-118">INTEGER</span></span>

<span data-ttu-id="73f64-119">Тег Encoding: 0x02</span><span class="sxs-lookup"><span data-stu-id="73f64-119">Encoding tag: 0x02</span></span>

<span data-ttu-id="73f64-120">Имя Certreq.exe: ЦЕЛОе число</span><span class="sxs-lookup"><span data-stu-id="73f64-120">Certreq.exe name: INTEGER</span></span>

<span data-ttu-id="73f64-121">Целочисленное значение обычно может быть любым положительным или отрицательным целочисленным значением.</span><span class="sxs-lookup"><span data-stu-id="73f64-121">An integer can typically be any positive or negative integral value.</span></span> <span data-ttu-id="73f64-122">В следующем примере показана структура ASN. 1 для открытого ключа RSA.</span><span class="sxs-lookup"><span data-stu-id="73f64-122">The following example shows the ASN.1 structure for an RSA public key.</span></span> <span data-ttu-id="73f64-123">Обратите внимание, что поле **публицекспонент** ограничивается положительным целым числом меньше 4 294 967 296.</span><span class="sxs-lookup"><span data-stu-id="73f64-123">Note that the **publicExponent** field is restricted to a positive integer less than 4,294,967,296.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: INTEGER
-- Tag number: 0x02
---------------------------------------------------------------------
HUGEINTEGER ::= INTEGER

RSAPublicKey ::= SEQUENCE 
{ 
  modulus         HUGEINTEGER,    
  publicExponent  INTEGER (0..4294967295) 
} 
```

## <a name="null"></a><span data-ttu-id="73f64-124">NULL</span><span class="sxs-lookup"><span data-stu-id="73f64-124">NULL</span></span>

<span data-ttu-id="73f64-125">Тег Encoding: 0x05</span><span class="sxs-lookup"><span data-stu-id="73f64-125">Encoding tag: 0x05</span></span>

<span data-ttu-id="73f64-126">Имя Certreq.exe: **null**</span><span class="sxs-lookup"><span data-stu-id="73f64-126">Certreq.exe name: **NULL**</span></span>

<span data-ttu-id="73f64-127">Тип **null** содержит один байт 0x00.</span><span class="sxs-lookup"><span data-stu-id="73f64-127">A **NULL** type contains a single byte 0x00.</span></span> <span data-ttu-id="73f64-128">Его можно использовать в любом месте, где запрос сертификата должен указывать на пустое значение.</span><span class="sxs-lookup"><span data-stu-id="73f64-128">It can be used anywhere that the certificate request must indicate an empty value.</span></span> <span data-ttu-id="73f64-129">Например, **алгорисмидентифиер** — это последовательность, которая содержит идентификатор объекта (OID) и необязательные параметры.</span><span class="sxs-lookup"><span data-stu-id="73f64-129">For example, an **AlgorithmIdentifier** is a sequence that contains an object identifier (OID) and optional parameters.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: NULL
-- Tag number: 0x05
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

<span data-ttu-id="73f64-130">Если при кодировании структуры нет параметров, для указания пустого значения используется **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="73f64-130">If there are no parameters when the structure is encoded, **NULL** is used to indicate an empty value.</span></span>

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a><span data-ttu-id="73f64-131">ИДЕНТИФИКАТОР ОБЪЕКТА</span><span class="sxs-lookup"><span data-stu-id="73f64-131">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="73f64-132">Тег Encoding: 0x06</span><span class="sxs-lookup"><span data-stu-id="73f64-132">Encoding tag: 0x06</span></span>

<span data-ttu-id="73f64-133">Имя Certreq.exe: \_ идентификатор объекта</span><span class="sxs-lookup"><span data-stu-id="73f64-133">Certreq.exe name: OBJECT\_ID</span></span>

<span data-ttu-id="73f64-134">API регистрации сертификатов использует идентификаторы объектов (OID) в качестве универсального указателя на идентификаторы алгоритма, атрибуты и другие элементы PKI.</span><span class="sxs-lookup"><span data-stu-id="73f64-134">The Certificate Enrollment API uses object identifiers (OIDs) as a type of universal pointer to algorithm identifiers, attributes, and other PKI elements.</span></span> <span data-ttu-id="73f64-135">OID обычно представлены в точечно-десятичной строке, например "2.16.840.1.101.3.4.1.42".</span><span class="sxs-lookup"><span data-stu-id="73f64-135">OIDs are typically presented in a dotted decimal string such as "2.16.840.1.101.3.4.1.42".</span></span> <span data-ttu-id="73f64-136">Отдельные элементы в строке, разделенные точками, представляют дуги и листья в дереве центра регистрации, которые однозначно идентифицируют объект и зарегистрированную в нем организацию.</span><span class="sxs-lookup"><span data-stu-id="73f64-136">The individual elements in the string, separated by periods, represent the arcs and leaves in a registration authority tree that uniquely identifies the object and the organization that registered it.</span></span> <span data-ttu-id="73f64-137">Например, предыдущий идентификатор объекта может быть расширен до совместного стандарта ISO-ITU-t (2) Country (16) US (840) (1) gov (101) КСОР (3) Нисталгорисмс (4) Аесалгс (1) с 256 добавлением. 42.</span><span class="sxs-lookup"><span data-stu-id="73f64-137">For example, the preceding OID can be expanded to joint-iso-itu-t(2) country(16) us(840) organization(1) gov(101) csor(3) nistAlgorithms(4) aesAlgs(1) with .42 appended to uniquely identify the 256-bit AES cipher block chaining (CBC) mode algorithm.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OBJECT IDENTIFIER
-- Tag number: 0x06
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="octet-string"></a><span data-ttu-id="73f64-138">СТРОКА ОКТЕТА</span><span class="sxs-lookup"><span data-stu-id="73f64-138">OCTET STRING</span></span>

<span data-ttu-id="73f64-139">Тег Encoding: 0x04</span><span class="sxs-lookup"><span data-stu-id="73f64-139">Encoding tag: 0x04</span></span>

<span data-ttu-id="73f64-140">Имя Certreq.exe: строка ОКТЕТа \_</span><span class="sxs-lookup"><span data-stu-id="73f64-140">Certreq.exe name: OCTET\_STRING</span></span>

<span data-ttu-id="73f64-141">Строка октета является произвольно большим массивом байтов.</span><span class="sxs-lookup"><span data-stu-id="73f64-141">An octet string is an arbitrarily large byte array.</span></span> <span data-ttu-id="73f64-142">Однако в отличие от типа **битовой строки** определенные биты и байты в строке не могут назначаться имена.</span><span class="sxs-lookup"><span data-stu-id="73f64-142">Unlike the **BIT STRING** type, however, specific bits and bytes in the string cannot be assigned names.</span></span> <span data-ttu-id="73f64-143">Слово «октет» предназначено для независимого от платформы способа ссылки на слово памяти.</span><span class="sxs-lookup"><span data-stu-id="73f64-143">The word octet is meant to be a platform independent way to refer to a memory word.</span></span> <span data-ttu-id="73f64-144">В контексте API регистрации сертификатов октет и Byte взаимозаменяемы.</span><span class="sxs-lookup"><span data-stu-id="73f64-144">Within the context of the Certificate Enrollment API, octet and byte are interchangeable.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OCTET STRING
-- Tag number: 0x04
---------------------------------------------------------------------
AuthorityKeyId ::= SEQUENCE 
{
  keyIdentifier       [0] IMPLICIT OCTET STRING OPTIONAL,
  certIssuer          [1] EXPLICIT NAME
  certSerialNumber    [2] IMPLICIT INTEGER OPTIONAL
}
```

## <a name="related-topics"></a><span data-ttu-id="73f64-145">См. также</span><span class="sxs-lookup"><span data-stu-id="73f64-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73f64-146">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="73f64-146">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="73f64-147">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="73f64-147">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="73f64-148">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="73f64-148">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



