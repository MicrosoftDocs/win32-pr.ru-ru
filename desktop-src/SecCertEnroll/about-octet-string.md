---
description: Тип данных строки ОКТЕТа ASN. 1 кодируется в TLV-Triplet, который начинается с тега Byte 0x04.
ms.assetid: 9d07a6c8-a15f-4030-838c-3063e315684f
title: СТРОКА ОКТЕТА
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2a042312a4415ea9554b7519404097287244f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497817"
---
# <a name="octet-string"></a><span data-ttu-id="9745c-103">СТРОКА ОКТЕТА</span><span class="sxs-lookup"><span data-stu-id="9745c-103">OCTET STRING</span></span>

<span data-ttu-id="9745c-104">Тип данных **строки октета** ASN. 1 кодируется в TLV-Triplet, который начинается с **тега** Byte 0x04.</span><span class="sxs-lookup"><span data-stu-id="9745c-104">The ASN.1 **OCTET STRING** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x04.</span></span> <span data-ttu-id="9745c-105">**Строка октета** и типы данных [битовой строки](about-bit-string.md) очень похожи.</span><span class="sxs-lookup"><span data-stu-id="9745c-105">The **OCTET STRING** and [BIT STRING](about-bit-string.md) data types are very similar.</span></span> <span data-ttu-id="9745c-106">Таким образом, два типа кодируются аналогичным образом за исключением того, что, поскольку замыкающий байт **строки октета** не может иметь неиспользуемые биты, в содержимое не должны добавляться начальные байты.</span><span class="sxs-lookup"><span data-stu-id="9745c-106">Thus, the two types are encoded in a similar manner except that, because the trailing byte of an **OCTET STRING** cannot have unused bits, no leading bytes must be added to the content.</span></span> <span data-ttu-id="9745c-107">В следующем примере, адаптированном из раздела [ASN. 1 в формате CMC](cmc-encoded-asn-1.md) , показано, как имя шаблона сертификата кодируется как массив байтов.</span><span class="sxs-lookup"><span data-stu-id="9745c-107">The following example, adapted from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows how the name of a certificate template is encoded as a byte array.</span></span>

``` syntax
30 17                                 ; SEQUENCE (17 Bytes)
|  06 09                              ; OBJECT_ID (9 Bytes)
|  |  2b 06 01 04 01 82 37 14  02     ;   1.3.6.1.4.1.311.20.2
|  04 0a                              ; OCTET_STRING (a Bytes)
|     1e 08 00 55 00 73 00 65  00 72  ;   ...U.s.e.r
```

<span data-ttu-id="9745c-108">Если массив байтов содержит менее 128 байт, поле **длины** TLV Triplet требует только одного байта для указания длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="9745c-108">If the byte array contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="9745c-109">Если его длина превышает 127 байт, в поле **length** в разряде 7 устанавливается значение 1, а для битов с 6 по 0 укажите число дополнительных байтов, используемых для определения длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="9745c-109">If it is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="9745c-110">Это показано в следующем примере, где бит высокого порядка второго байта в первой строке имеет значение 1, а байт указывает на наличие байта конечной **длины** .</span><span class="sxs-lookup"><span data-stu-id="9745c-110">This is shown in the following example where the high order bit of the second byte on the first line is set to 1 and the byte indicates that there is a trailing **Length** byte.</span></span> <span data-ttu-id="9745c-111">Следовательно, третий байт указывает, что содержимое имеет длину в 0x80 байт.</span><span class="sxs-lookup"><span data-stu-id="9745c-111">The third byte therefore specifies that the content is 0x80 bytes long.</span></span>

``` syntax
04 81 80                       ; OCTET_STRING (80 Bytes)
   38 10 60 e2 70 69 91 4a     ;   8.`.pi.J
   8b b5 22 57 2a 62 ef de     ;   .."W*b..
   15 7d 59 d6 4e 20 9a 45     ;   .}Y.N .E
   2b e3 fd fc 68 ba af bf     ;   +...h...
   9c 17 b0 8e 6d c4 29 1e     ;   ....m.).
   e3 21 ac bb 5a 8a c9 67     ;   .!..Z..g
   0a d4 45 93 10 c0 26 eb     ;   ..E...&.
   0a 83 c2 b1 40 87 36 f7     ;   ....@.6.
   a0 26 da b9 bb 46 73 88     ;   .&...Fs.
   7a 67 b9 e6 b3 6f ea 59     ;   zg...o.Y
   28 8a d3 92 72 f6 7b 89     ;   (...r.{.
   a0 d8 2d 9e 40 eb 1e bb     ;   ..-.@...
   6e ae f0 5a ed 16 c9 e3     ;   n..Z....
   27 59 37 8f f3 4a 98 60     ;   'Y7..J.`
   f8 fb a7 0a ee 1b 6e 91     ;   ......n.
   95 96 cf 0d 56 ac ab 35     ;   ....V..5
```

## <a name="related-topics"></a><span data-ttu-id="9745c-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9745c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9745c-113">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="9745c-113">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="9745c-114">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="9745c-114">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



