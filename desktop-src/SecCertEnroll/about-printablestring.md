---
description: Тип данных ASN. 1 Принтаблестринг кодируется в TLV-Triplet, который начинается с тега Byte 0x13.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: принтаблестринг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ebc95f1a58e8d7beb4a1d3bbb037788252349a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909643"
---
# <a name="printablestring"></a><span data-ttu-id="3ad39-103">принтаблестринг</span><span class="sxs-lookup"><span data-stu-id="3ad39-103">PrintableString</span></span>

<span data-ttu-id="3ad39-104">Тип данных ASN. 1 **принтаблестринг** кодируется в TLV-Triplet, который начинается с **тега** Byte 0x13.</span><span class="sxs-lookup"><span data-stu-id="3ad39-104">The ASN.1 **PrintableString** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x13.</span></span> <span data-ttu-id="3ad39-105">В следующем примере из статьи [PKCS \# 10 Encoded ASN. 1](pkcs--10-encoded-asn-1.md) показано, как общее имя пользователя тесткн кодируется как тип **принтаблестринг** .</span><span class="sxs-lookup"><span data-stu-id="3ad39-105">The following example, from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic, shows how a user common name of TestCN is encoded as a **PrintableString** type.</span></span> <span data-ttu-id="3ad39-106">Идентификатор объекта для общего имени — 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="3ad39-106">The object identifier for a common name is 2.5.4.3.</span></span>

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

<span data-ttu-id="3ad39-107">Если строка содержит менее 128 байт, то поле **length** TLV Triplet требует только одного байта для указания длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="3ad39-107">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="3ad39-108">Если длина строки превышает 127 байт, то разряд 7 в поле **length** устанавливается в 1, а биты с 6 по 0 указывают количество дополнительных байтов, используемых для определения длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="3ad39-108">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="3ad39-109">Дополнительные сведения см. в разделе [кодированная Длина и байты значений](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="3ad39-109">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ad39-110">См. также</span><span class="sxs-lookup"><span data-stu-id="3ad39-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ad39-111">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="3ad39-111">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="3ad39-112">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="3ad39-112">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



