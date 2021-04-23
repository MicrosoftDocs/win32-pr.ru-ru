---
description: Тип данных BIT STRING кодируется в TLV-Triplet, который начинается с тега Byte 0x03.
ms.assetid: 7464dd20-5e79-4ca1-a6ae-9b706e9cb925
title: БИТОВАЯ СТРОКА
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115ead46663b94d6db2d089f1fae2fd8c40a2ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571634"
---
# <a name="bit-string"></a><span data-ttu-id="ffd45-103">БИТОВАЯ СТРОКА</span><span class="sxs-lookup"><span data-stu-id="ffd45-103">BIT STRING</span></span>

<span data-ttu-id="ffd45-104">Тип данных **bit String** кодируется в TLV-Triplet, который начинается с **тега** Byte 0x03.</span><span class="sxs-lookup"><span data-stu-id="ffd45-104">The **BIT STRING** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x03.</span></span> <span data-ttu-id="ffd45-105">Поле **значения** TLV Triplet содержит начальный байт, указывающий количество неиспользованных битов в последнем байте содержимого.</span><span class="sxs-lookup"><span data-stu-id="ffd45-105">The **Value** field of the TLV triplet contains a leading byte that specifies the number of bits left unused in the final byte of content.</span></span> <span data-ttu-id="ffd45-106">В следующем примере поле **length** имеет значение 0x03, так как после трех байтов содержимого соблюдается **значение 0x04** , поскольку в последнем байте содержимого содержится четыре неиспользуемых бита.</span><span class="sxs-lookup"><span data-stu-id="ffd45-106">In the following example, the **Length** field is set to 0x03 because three content bytes follow, and the leading byte of the **Value** field is set to 0x04 because there are four unused bits in the last content byte.</span></span> <span data-ttu-id="ffd45-107">Каждый неиспользованный бит обозначается буквой x.</span><span class="sxs-lookup"><span data-stu-id="ffd45-107">Each unused bit is denoted by the letter x.</span></span>

![Кодировка der для строковых данных типа bit](images/der-tlv-bitstring.png)

<span data-ttu-id="ffd45-109">В следующем примере, адаптированном из раздела [PKCS \# 10 Encoded ASN. 1](pkcs--10-encoded-asn-1.md) , показана закодированная подпись примера запроса на сертификат PKCS \# 10.</span><span class="sxs-lookup"><span data-stu-id="ffd45-109">The following example, adapted from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic, shows the encoded signature of a sample PKCS \#10 certificate request.</span></span> <span data-ttu-id="ffd45-110">Первый байт содержит значение **тега** для типа данных **bit String** , 0x03.</span><span class="sxs-lookup"><span data-stu-id="ffd45-110">The first byte contains the **Tag** value for the **BIT STRING** data type, 0x03.</span></span> <span data-ttu-id="ffd45-111">Второй и третий байты содержат длину массива байтов.</span><span class="sxs-lookup"><span data-stu-id="ffd45-111">The second and third bytes contain the length of the byte array.</span></span> <span data-ttu-id="ffd45-112">Бит 7 второго байта равен 1, так как имеется более 127 байт содержимого.</span><span class="sxs-lookup"><span data-stu-id="ffd45-112">Bit 7 of the second byte is set to 1 because there are more than 127 bytes of content.</span></span> <span data-ttu-id="ffd45-113">Биты от 0 до 6 второго байта указывают количество конечных **байтов в** конце (в данном случае).</span><span class="sxs-lookup"><span data-stu-id="ffd45-113">Bits 0 through 6 of the second byte specify the number of trailing **Length** bytes, in this case one.</span></span> <span data-ttu-id="ffd45-114">Третий байт указывает число байтов содержимого, 0x81.</span><span class="sxs-lookup"><span data-stu-id="ffd45-114">The third byte specifies the number of content bytes, 0x81.</span></span> <span data-ttu-id="ffd45-115">Четвертый байт 0x00 указывает количество неиспользованных битов, существующих в последнем байте содержимого.</span><span class="sxs-lookup"><span data-stu-id="ffd45-115">The fourth byte, 0x00, specifies the number of unused bits that exist in the last content byte.</span></span> <span data-ttu-id="ffd45-116">Обратите внимание, что сигнатура кодируется в порядке байтов с обратным порядком.</span><span class="sxs-lookup"><span data-stu-id="ffd45-116">Note that the signature is encoded in big-endian byte order.</span></span>

``` syntax
0299:    03 81 81           ; BIT_STRING (81 Bytes)
029c:       00
029d:       47 eb 99 5a df 9e 70 0d  fb a7 31 32 c1 5f 5c 24
02ad:       c2 e0 bf c6 24 af 15 66  0e b8 6a 2e ab 2b c4 97
02bd:       1f e3 cb dc 63 a5 25 ec  c7 b4 28 61 66 36 a1 31
02cd:       1b bf dd d0 fc bf 17 94  90 1d e5 5e c7 11 5e c9
02dd:       55 9f eb a3 3e 14 c7 99  a6 cb ba a1 46 0f 39 d4
02ed:       44 c4 c8 4b 76 0e 20 5d  6d a9 34 9e d4 d5 87 42
02fd:       eb 24 26 51 14 90 b4 0f  06 5e 52 88 32 7a 95 20
030d:       a0 fd f7 e5 7d 60 dd 72  68 9b f5 7b 05 8f 6d 1e
```

## <a name="related-topics"></a><span data-ttu-id="ffd45-117">См. также</span><span class="sxs-lookup"><span data-stu-id="ffd45-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffd45-118">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="ffd45-118">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="ffd45-119">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="ffd45-119">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="ffd45-120">Закодированная Длина и байты значений</span><span class="sxs-lookup"><span data-stu-id="ffd45-120">Encoded Length and Value Bytes</span></span>](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 



