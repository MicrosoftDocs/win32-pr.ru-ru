---
description: Целочисленные значения кодируются в TLV-Triplet, который начинается с значения тега 0x02.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: ЦЕЛОе число (API регистрации сертификатов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0e8ed162d4cf4b2ac4909baf1cd7b5e94ddea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345435"
---
# <a name="integer-certificate-enrollment-api"></a><span data-ttu-id="45273-103">ЦЕЛОе число (API регистрации сертификатов)</span><span class="sxs-lookup"><span data-stu-id="45273-103">INTEGER (Certificate Enrollment API)</span></span>

<span data-ttu-id="45273-104">Целочисленные значения кодируются в TLV-Triplet, который начинается с значения **тега** 0x02.</span><span class="sxs-lookup"><span data-stu-id="45273-104">Integer values are encoded into a TLV triplet that begins with a **Tag** value of 0x02.</span></span> <span data-ttu-id="45273-105">Поле **значения** TLV Triplet содержит закодированное целое число, если оно положительное, или его дополнение, если оно отрицательное.</span><span class="sxs-lookup"><span data-stu-id="45273-105">The **Value** field of the TLV triplet contains the encoded integer if it is positive, or its two's complement if it is negative.</span></span> <span data-ttu-id="45273-106">Если целое число положительное, а бит высокого порядка имеет значение 1, в содержимое добавляется ведущий 0x00, чтобы указать, что число не является отрицательным.</span><span class="sxs-lookup"><span data-stu-id="45273-106">If the integer is positive but the high order bit is set to 1, a leading 0x00 is added to the content to indicate that the number is not negative.</span></span> <span data-ttu-id="45273-107">Например, байт высокого порядка в 0x8F (10001111) равен 1.</span><span class="sxs-lookup"><span data-stu-id="45273-107">For example, the high order byte of 0x8F (10001111) is 1.</span></span> <span data-ttu-id="45273-108">Таким образом, в содержимое добавляется начальный нуль-байт, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="45273-108">Therefore a leading zero byte is added to the content as shown in the following illustration.</span></span>

![Кодировка der логического типа данных](images/der-tlv-integer.png)

<span data-ttu-id="45273-110">Если целое число содержит менее 128 байт, поле *length* должно содержать только один байт для указания длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="45273-110">If the integer contains fewer than 128 bytes, the *Length* field requires only one byte to specify the content length.</span></span> <span data-ttu-id="45273-111">Если целое число превышает 127 байт, в поле *length* в разряде 7 устанавливается значение 1, а для битов с 6 по 0 укажите число дополнительных байтов, используемых для определения длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="45273-111">If the integer is more than 127 bytes, bit 7 of the *Length* field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="45273-112">Дополнительные сведения см. в разделе [кодированная Длина и байты значений](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="45273-112">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

<span data-ttu-id="45273-113">В следующем примере из [PKCS \# 10 с кодировкой ASN. 1](pkcs--10-encoded-asn-1.md)показана кодировка для открытого ключа 128 байта.</span><span class="sxs-lookup"><span data-stu-id="45273-113">The following example, from [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md), shows the encoding for a 128 byte public key.</span></span> <span data-ttu-id="45273-114">Первый байт содержит значение **тега** для **целочисленного** типа данных, 0x02.</span><span class="sxs-lookup"><span data-stu-id="45273-114">The first byte contains the **Tag** value for the **INTEGER** data type, 0x02.</span></span> <span data-ttu-id="45273-115">Второй и третий байты содержат значение **длины** .</span><span class="sxs-lookup"><span data-stu-id="45273-115">The second and third bytes contain the **Length** value.</span></span> <span data-ttu-id="45273-116">Бит 7 второго байта равен 1, так как имеется более 127 байт содержимого.</span><span class="sxs-lookup"><span data-stu-id="45273-116">Bit 7 of the second byte is set to 1 because there are more than 127 bytes of content.</span></span> <span data-ttu-id="45273-117">Биты от 0 до 6 второго байта указывают количество требуемых конечных байтов, в данном случае один — для точного указания длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="45273-117">Bits 0 through 6 of the second byte specify the number of trailing bytes needed, in this case one, to accurately specify the content length.</span></span> <span data-ttu-id="45273-118">Третий байт указывает число байтов содержимого, 0x81.</span><span class="sxs-lookup"><span data-stu-id="45273-118">The third byte specifies the number of content bytes, 0x81.</span></span> <span data-ttu-id="45273-119">Четвертый байт 0x00 добавляется к содержимому, чтобы указать, что целое число действительно является положительным значением, хотя бит знака ведущего содержимого (0x8F) имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="45273-119">The fourth byte, 0x00, is added to the content to indicate that the integer is indeed a positive value even though the sign bit of the leading content byte (0x8F) is set to 1.</span></span>

``` syntax
02 81 81          ; INTEGER (81 Bytes)
|  00
|  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
```

<span data-ttu-id="45273-120">В следующем примере показано, как кодируется целочисленное значение 0x03.</span><span class="sxs-lookup"><span data-stu-id="45273-120">The following example shows how the integer value 0x03 is encoded.</span></span> <span data-ttu-id="45273-121">Байт **тега** содержит 0x02, а **Длина** байта указывает на один байт содержимого.</span><span class="sxs-lookup"><span data-stu-id="45273-121">The **Tag** byte contains 0x02, and the **Length** byte specifies that there is one byte of content.</span></span>

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a><span data-ttu-id="45273-122">См. также</span><span class="sxs-lookup"><span data-stu-id="45273-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45273-123">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="45273-123">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="45273-124">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="45273-124">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



