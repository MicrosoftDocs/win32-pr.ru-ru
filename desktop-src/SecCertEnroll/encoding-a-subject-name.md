---
description: При инициализации объекта IX500DistinguishedName с различающимся именем для указания субъекта запроса на сертификат создается Distinguished Encoding Rules (DER) синтаксическая нотация (ASN. 1).
ms.assetid: 58b05b59-2235-49bd-9543-45e786d62eaf
title: Кодирование имени субъекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa03d95497a600c3e61fdda53820fd7a9858c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080355"
---
# <a name="encoding-a-subject-name"></a><span data-ttu-id="b72fe-103">Кодирование имени субъекта</span><span class="sxs-lookup"><span data-stu-id="b72fe-103">Encoding a Subject Name</span></span>

<span data-ttu-id="b72fe-104">При инициализации объекта [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) с различающимся именем для указания субъекта запроса на сертификат создается [*distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (Der) [*синтаксическая нотация*](/windows/desktop/SecGloss/a-gly) (ASN. 1).</span><span class="sxs-lookup"><span data-stu-id="b72fe-104">When you initialize an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object with a distinguished name to identify the subject of a certificate request, a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) sequence is created.</span></span> <span data-ttu-id="b72fe-105">Например, предположим, что различающееся имя субъекта состоит из следующих относительных различающихся имен (Рднс):</span><span class="sxs-lookup"><span data-stu-id="b72fe-105">For example, assume that the subject distinguished name consists of the following relative distinguished names (RDNs):</span></span><dl> <span data-ttu-id="b72fe-106">E =Administrator@jdomcsc.nttest.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b72fe-106">E=Administrator@jdomcsc.nttest.microsoft.com</span></span>  
<span data-ttu-id="b72fe-107">CN = администратор</span><span class="sxs-lookup"><span data-stu-id="b72fe-107">CN=Administrator</span></span>  
<span data-ttu-id="b72fe-108">CN = пользователи</span><span class="sxs-lookup"><span data-stu-id="b72fe-108">CN=Users</span></span>  
<span data-ttu-id="b72fe-109">DC = ждомкск</span><span class="sxs-lookup"><span data-stu-id="b72fe-109">DC=jdomcsc</span></span>  
<span data-ttu-id="b72fe-110">DC = нттест</span><span class="sxs-lookup"><span data-stu-id="b72fe-110">DC=nttest</span></span>  
<span data-ttu-id="b72fe-111">DC = Microsoft</span><span class="sxs-lookup"><span data-stu-id="b72fe-111">DC=microsoft</span></span>  
<span data-ttu-id="b72fe-112">DC = com</span><span class="sxs-lookup"><span data-stu-id="b72fe-112">DC=com</span></span>  
<span data-ttu-id="b72fe-113"></dl>The **IX500DistinguishedName** object creates the following DER-encoded (ASN.1) sequence. Notice that the sequence is encoded in reverse order. This example is derived from the<a href="pkcs--7-renewal-encoded-asn-1.md">Обновление PKCS #7 с кодировкой ASN. 1</a> .</span><span class="sxs-lookup"><span data-stu-id="b72fe-113"></dl>The **IX500DistinguishedName** object creates the following DER-encoded (ASN.1) sequence. Notice that the sequence is encoded in reverse order. This example is derived from the<a href="pkcs--7-renewal-encoded-asn-1.md">PKCS #7 Renewal Encoded ASN.1</a> topic.</span></span>

``` syntax
0a0d: 30 81 c4          ; SEQUENCE (c4 Bytes)
0a10: |  31 13          ; SET (13 Bytes)
0a12: |  |  30 11               ; SEQUENCE (11 Bytes)
0a14: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a16: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a20: |  |     16 03        ; IA5_STRING (3 Bytes)
0a22: |  |        63 6f 6d                                          ; com
      |  |           ; "com"
0a25: |  31 19          ; SET (19 Bytes)
0a27: |  |  30 17               ; SEQUENCE (17 Bytes)
0a29: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a2b: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a35: |  |     16 09            ; IA5_STRING (9 Bytes)
0a37: |  |        6d 69 63 72 6f 73 6f 66  74                       ; microsoft
      |  |           ; "microsoft"
0a40: |  31 16          ; SET (16 Bytes)
0a42: |  |  30 14               ; SEQUENCE (14 Bytes)
0a44: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a46: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a50: |  |     16 06            ; IA5_STRING (6 Bytes)
0a52: |  |        6e 74 74 65 73 74                                 ; nttest
      |  |           ; "nttest"
0a58: |  31 17          ; SET (17 Bytes)
0a5a: |  |  30 15               ; SEQUENCE (15 Bytes)
0a5c: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a5e: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a68: |  |     16 07            ; IA5_STRING (7 Bytes)
0a6a: |  |        6a 64 6f 6d 63 73 63                              ; jdomcsc
      |  |           ; "jdomcsc"
0a71: |  31 0e          ; SET (e Bytes)
0a73: |  |  30 0c               ; SEQUENCE (c Bytes)
0a75: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a77: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a7a: |  |     13 05            ; PRINTABLE_STRING (5 Bytes)
0a7c: |  |        55 73 65 72 73                                    ; Users
      |  |           ; "Users"
0a81: |  31 16          ; SET (16 Bytes)
0a83: |  |  30 14               ; SEQUENCE (14 Bytes)
0a85: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a87: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a8a: |  |     13 0d            ; PRINTABLE_STRING (d Bytes)
0a8c: |  |        41 64 6d 69 6e 69 73 74  72 61 74 6f 72           ; Administrator
      |  |           ; "Administrator"
0a99: |  31 39          ; SET (39 Bytes)
0a9b: |     30 37               ; SEQUENCE (37 Bytes)
0a9d: |        06 09            ; OBJECT_ID (9 Bytes)
0a9f: |        |  2a 86 48 86 f7 0d 01 09  01
      |        |     ; 1.2.840.113549.1.9.1 Email Address (E)
0aa8: |        16 2a            ; IA5_STRING (2a Bytes)
0aaa: |           41 64 6d 69 6e 69 73 74  72 61 74 6f 72 40 6a 64  ; Administrator@jd
0aba: |           6f 6d 63 73 63 2e 6e 74  74 65 73 74 2e 6d 69 63  ; omcsc.nttest.mic
0aca: |           72 6f 73 6f 66 74 2e 63  6f 6d                    ; rosoft.com
      |              ; "Administrator@jdomcsc.nttest.microsoft.com"
```

<span data-ttu-id="b72fe-114">Как обсуждалось в [именах субъектов](subject-names.md), каждый RDN в различающемся имени состоит из набора атрибутов, а каждый атрибут содержит [*идентификатор объекта*](/windows/desktop/SecGloss/o-gly) (OID) и значение.</span><span class="sxs-lookup"><span data-stu-id="b72fe-114">As discussed in [Subject Names](subject-names.md), every RDN in a distinguished name consists of a set of attributes, and each attribute contains an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) and a value.</span></span> <span data-ttu-id="b72fe-115">Чтобы понять, как объект [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) кодирует различающееся имя, рассмотрите общее имя CN = Users.</span><span class="sxs-lookup"><span data-stu-id="b72fe-115">To understand how the [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object encodes a distinguished name, consider the common name CN=Users.</span></span>

``` syntax
0a73: |  |  30 0c               ; SEQUENCE (c Bytes)
0a75: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a77: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a7a: |  |     13 05            ; PRINTABLE_STRING (5 Bytes)
0a7c: |  |        55 73 65 72 73                                    ; Users
      |  |           ; "Users"
```

<span data-ttu-id="b72fe-116">Синтаксис обмена в формате DER объекта ASN. 1 всегда содержит тип, длину и значение Triplet, а каждое поле в Triplet содержит один или несколько байтов.</span><span class="sxs-lookup"><span data-stu-id="b72fe-116">The DER transfer syntax of an ASN.1 object always contains a type, length, and value triplet, and each field in the triplet contains one or more bytes.</span></span> <span data-ttu-id="b72fe-117">При кодировании CN = Users состоит из OID и строкового значения.</span><span class="sxs-lookup"><span data-stu-id="b72fe-117">When encoded, CN=Users consists of an OID and a string value.</span></span> <span data-ttu-id="b72fe-118">Точечно-десятичная нотация OID CN — 2.5.4.3, а строковое значение — «Users».</span><span class="sxs-lookup"><span data-stu-id="b72fe-118">The dotted decimal notation of the CN OID is 2.5.4.3 and the string value is "Users".</span></span> <span data-ttu-id="b72fe-119">Строковое значение представлено как тип данных **PRINTABLE_STRING** .</span><span class="sxs-lookup"><span data-stu-id="b72fe-119">The string value is represented as a **PRINTABLE_STRING** data type.</span></span> <span data-ttu-id="b72fe-120">Значение числового типа, связанное с **object_id** , всегда равно 0x06, а числовой тип, связанный с **PRINTABLE_STRING** , всегда является 0x13.</span><span class="sxs-lookup"><span data-stu-id="b72fe-120">The numeric type value associated with **OBJECT_ID** is always 0x06, and the numeric type associated with **PRINTABLE_STRING** is always 0x13.</span></span> <span data-ttu-id="b72fe-121">Длина общего имени "Users" — 0x05 байт.</span><span class="sxs-lookup"><span data-stu-id="b72fe-121">The length of the common name "Users" is 0x05 bytes.</span></span> <span data-ttu-id="b72fe-122">Длина OID равна 0x03 байтам, а значение — 0x55 0x04 0x03.</span><span class="sxs-lookup"><span data-stu-id="b72fe-122">The length of the OID is 0x03 bytes, and it's value is 0x55 0x04 0x03.</span></span>

> [!Note]  
> <span data-ttu-id="b72fe-123">Чтобы перевести первые две цифры OID 2.5.4.3 в шестнадцатеричное значение 0x55, умножьте первую цифру OID на 40 (2 x 40) и добавьте вторую цифру (5) перед преобразованием в шестнадцатеричный формат.</span><span class="sxs-lookup"><span data-stu-id="b72fe-123">To translate the first two digits of the OID 2.5.4.3 into the hexadecimal value 0x55, multiply the first digit of the OID by 40 (2 x 40) and add the second digit (5) before converting to hexadecimal.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b72fe-124">См. также</span><span class="sxs-lookup"><span data-stu-id="b72fe-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b72fe-125">\#Обновление PKCS 7 с кодировкой ASN. 1</span><span class="sxs-lookup"><span data-stu-id="b72fe-125">PKCS \#7 Renewal Encoded ASN.1</span></span>](pkcs--7-renewal-encoded-asn-1.md)
</dt> <dt>

[<span data-ttu-id="b72fe-126">Примеры запросов</span><span class="sxs-lookup"><span data-stu-id="b72fe-126">Sample Requests</span></span>](sample-requests.md)
</dt> <dt>

[<span data-ttu-id="b72fe-127">Имена субъектов</span><span class="sxs-lookup"><span data-stu-id="b72fe-127">Subject Names</span></span>](subject-names.md)
</dt> </dl>

 

 
