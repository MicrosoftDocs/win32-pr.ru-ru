---
description: API регистрации сертификатов использует синтаксическую нотацию 1 (ASN. 1) для определения, кодирования и декодирования запросов сертификатов и сертификатов, передаваемых между клиентскими компьютерами и центрами сертификации.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Общие сведения о синтаксисе и кодировке ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4fe15d2fb8fba4af25b9da7c249fec3a92630e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909648"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a><span data-ttu-id="8c491-103">Общие сведения о синтаксисе и кодировке ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8c491-103">Introduction to ASN.1 Syntax and Encoding</span></span>

<span data-ttu-id="8c491-104">API регистрации сертификатов использует синтаксическую нотацию 1 (ASN. 1) для определения, кодирования и декодирования запросов сертификатов и сертификатов, передаваемых между клиентскими компьютерами и центрами сертификации.</span><span class="sxs-lookup"><span data-stu-id="8c491-104">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to define, encode, and decode the certificate requests and certificates that it transfers between client computers and certification authorities.</span></span> <span data-ttu-id="8c491-105">ASN. 1 можно концептуально разделить на набор синтаксических правил и набор правил кодирования, как показано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="8c491-105">ASN.1 can be conceptually divided into a set of syntax rules and a set of encoding rules as shown by the following examples.</span></span>

## <a name="asn1-syntax-example"></a><span data-ttu-id="8c491-106">Пример синтаксиса ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8c491-106">ASN.1 Syntax Example</span></span>

<span data-ttu-id="8c491-107">Запрос на сертификат содержит, помимо прочего, имя сущности, которая делает запрос или для которого выполняется запрос.</span><span class="sxs-lookup"><span data-stu-id="8c491-107">A certificate request contains, among other things, the name of the entity that is making the request or for which the request is being made.</span></span> <span data-ttu-id="8c491-108">Имя представляет собой последовательность относительного различающегося имени X. 500 (Рднс).</span><span class="sxs-lookup"><span data-stu-id="8c491-108">The name is a sequence of X.500 relative distinguished names (RDNs).</span></span> <span data-ttu-id="8c491-109">Каждое RDN в последовательности состоит из идентификатора объекта (OID) и значения.</span><span class="sxs-lookup"><span data-stu-id="8c491-109">Each RDN in the sequence consists of an object identifier (OID) and a value.</span></span> <span data-ttu-id="8c491-110">В следующем примере показан синтаксис ASN. 1 для имени субъекта.</span><span class="sxs-lookup"><span data-stu-id="8c491-110">The ASN.1 syntax for a subject name is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Subject name
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}
```

## <a name="asn1-encoding-example"></a><span data-ttu-id="8c491-111">Пример кодировки ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8c491-111">ASN.1 Encoding Example</span></span>

<span data-ttu-id="8c491-112">API регистрации сертификатов использует [*distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (Der) для кодирования предыдущего имени субъекта.</span><span class="sxs-lookup"><span data-stu-id="8c491-112">The Certificate Enrollment API uses [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) to encode the preceding subject name.</span></span> <span data-ttu-id="8c491-113">DER требует, чтобы каждый элемент в имени представлялся TLV-Triplet, где T содержит номер тега типа ASN. 1, L содержит длину, а V содержит связанное значение.</span><span class="sxs-lookup"><span data-stu-id="8c491-113">DER requires that each item in the name be represented by a TLV triplet where T contains the tag number of the ASN.1 type, L contains the length, and V contains the associated value.</span></span> <span data-ttu-id="8c491-114">В следующем примере показано, как кодируется имя субъекта Тесткн. Тесторг.</span><span class="sxs-lookup"><span data-stu-id="8c491-114">The following example shows how the subject name TestCN.TestOrg is encoded.</span></span>

``` syntax
1.     30 23            ; SEQUENCE (23 Bytes)
2.     |  |  31 0f            ; SET (f Bytes)
3.     |  |  |  30 0d            ; SEQUENCE (d Bytes)
4.     |  |  |     06 03         ; OBJECT_ID (3 Bytes)
5.     |  |  |     |  55 04 03
6.     |  |  |     |     ; 2.5.4.3 Common Name (CN)
7.     |  |  |     13 06         ; PRINTABLE_STRING (6 Bytes)
8.     |  |  |        54 65 73 74 43 4e                    ; TestCN
9.     |  |  |           ; "TestCN"
10.    |  |  31 10            ; SET (10 Bytes)
11.    |  |     30 0e            ; SEQUENCE (e Bytes)
12.    |  |        06 03         ; OBJECT_ID (3 Bytes)
13.    |  |        |  55 04 0a
14.    |  |        |     ; 2.5.4.10 Organization (O)
15.    |  |        13 07         ; PRINTABLE_STRING (7 Bytes)
16.    |  |           54 65 73 74 4f 72 67                 ; TestOrg
17.    |  |              ; "TestOrg"
```

<span data-ttu-id="8c491-115">Обратите внимание на следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="8c491-115">Note the following points:</span></span>

-   <span data-ttu-id="8c491-116">Строка 1:</span><span class="sxs-lookup"><span data-stu-id="8c491-116">Line 1:</span></span><dl> <span data-ttu-id="8c491-117">Имя представляет собой последовательность относительных различающихся имен.</span><span class="sxs-lookup"><span data-stu-id="8c491-117">The name is a sequence of relative distinguished names.</span></span>  
    <span data-ttu-id="8c491-118">Номер тега для типа **последовательности** — 0x30.</span><span class="sxs-lookup"><span data-stu-id="8c491-118">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="8c491-119">Для имени субъекта Тесткн. Тесторг требуется 35 (0x23) байт.</span><span class="sxs-lookup"><span data-stu-id="8c491-119">The subject name of TestCN.TestOrg requires 35 (0x23) bytes.</span></span>  
    </dl>
-   Line 2:<dl> <span data-ttu-id="8c491-120">Общее имя, Тесткн, является единым набором структур **аттрибутетипевалуе** .</span><span class="sxs-lookup"><span data-stu-id="8c491-120">The Common Name, TestCN, is a single set of **AttributeTypeValue** structures.</span></span>  
    <span data-ttu-id="8c491-121">Номер тега для **набора** — 0x31.</span><span class="sxs-lookup"><span data-stu-id="8c491-121">The tag number for a **SET** is 0x31.</span></span>  
    </dl><span data-ttu-id="8c491-122">
-   Строка 3:</span><span class="sxs-lookup"><span data-stu-id="8c491-122">
-   Line 3:</span></span><dl> <span data-ttu-id="8c491-123">Структура **аттрибутетипевалуе** является последовательностью.</span><span class="sxs-lookup"><span data-stu-id="8c491-123">The **AttributeTypeValue** structure is a sequence.</span></span>  
    <span data-ttu-id="8c491-124">Номер тега для типа **последовательности** — 0x30.</span><span class="sxs-lookup"><span data-stu-id="8c491-124">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="8c491-125">Для этой структуры требуется 13 (0xD) байт.</span><span class="sxs-lookup"><span data-stu-id="8c491-125">The structure requires 13 (0xD) bytes.</span></span>  
    </dl><span data-ttu-id="8c491-126">
-   Строки с 4 по 6:</span><span class="sxs-lookup"><span data-stu-id="8c491-126">
-   Lines 4 to 6:</span></span><dl> <span data-ttu-id="8c491-127">Идентификатор объекта (OID) для общего имени — 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="8c491-127">The object identifier (OID) for the Common Name is 2.5.4.3.</span></span>  
    <span data-ttu-id="8c491-128">OID является типом **\_ идентификатора объекта** в три байта.</span><span class="sxs-lookup"><span data-stu-id="8c491-128">The OID is a three byte **OBJECT\_ID** type.</span></span>  
    <span data-ttu-id="8c491-129">Номер тега для типа **\_ идентификатора объекта** — 0x06.</span><span class="sxs-lookup"><span data-stu-id="8c491-129">The tag number for the **OBJECT\_ID** type is 0x06.</span></span>  
    </dl><span data-ttu-id="8c491-130">
-   Строки 7 – 9:</span><span class="sxs-lookup"><span data-stu-id="8c491-130">
-   Lines 7 to 9:</span></span><dl> <span data-ttu-id="8c491-131">Общее имя, Тесткн, является строковым значением.</span><span class="sxs-lookup"><span data-stu-id="8c491-131">The Common Name, TestCN, is a string value.</span></span>  
    <span data-ttu-id="8c491-132">Строка является шестью байтами **печатаемого \_ строкового** типа.</span><span class="sxs-lookup"><span data-stu-id="8c491-132">The string is a six byte **PRINTABLE\_STRING** type.</span></span>  
    <span data-ttu-id="8c491-133">Номер тега для **печатного типа \_ строки** — 0x13.</span><span class="sxs-lookup"><span data-stu-id="8c491-133">The tag number for the **PRINTABLE\_STRING** type is 0x13.</span></span>  
    </dl>

## <a name="related-topics"></a><span data-ttu-id="8c491-134">См. также</span><span class="sxs-lookup"><span data-stu-id="8c491-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c491-135">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8c491-135">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="8c491-136">Кодирование запроса сертификата</span><span class="sxs-lookup"><span data-stu-id="8c491-136">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="8c491-137">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8c491-137">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="8c491-138">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="8c491-138">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 
