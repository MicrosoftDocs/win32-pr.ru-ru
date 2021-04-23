---
description: Тип данных ASN. 1 IA5tring кодируется в TLV-Triplet, который начинается с тега Byte 0x16.
ms.assetid: c1268524-4304-4c21-8f7d-f0a2826cd74e
title: IA5String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7562fab655462455b03d35041bdb8f572b064cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264487"
---
# <a name="ia5string"></a><span data-ttu-id="7a32e-103">IA5String</span><span class="sxs-lookup"><span data-stu-id="7a32e-103">IA5String</span></span>

<span data-ttu-id="7a32e-104">Тип данных ASN. 1 **IA5tring** кодируется в TLV-Triplet, который начинается с **тега** Byte 0x16.</span><span class="sxs-lookup"><span data-stu-id="7a32e-104">The ASN.1 **IA5tring** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x16.</span></span> <span data-ttu-id="7a32e-105">В следующем примере, адаптированном из раздела [ASN. 1 в формате CMC](cmc-encoded-asn-1.md) , показано, как атрибут **OSVersion** кодируется как тип **IA5tring** .</span><span class="sxs-lookup"><span data-stu-id="7a32e-105">The following example, adapted from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows how the **OSVersion** attribute is encoded as an **IA5tring** type.</span></span> <span data-ttu-id="7a32e-106">Номер версии можно указать с помощью интерфейса [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) .</span><span class="sxs-lookup"><span data-stu-id="7a32e-106">The version number can be specified by using the [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) interface.</span></span> <span data-ttu-id="7a32e-107">Идентификатор объекта для атрибута — 1.3.6.1.4.1.311.13.2.3.</span><span class="sxs-lookup"><span data-stu-id="7a32e-107">The object identifier for the attribute is 1.3.6.1.4.1.311.13.2.3.</span></span>

``` syntax
06 0a                                   ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 03       ;   1.3.6.1.4.1.311.13.2.3 
31 0c                                   ; SET (c Bytes)
   16 0a                                ; IA5_STRING (a Bytes)
      36 2e 30 2e 35 33 36 31  2e 32    ;   6.0.5361.2
```

<span data-ttu-id="7a32e-108">Если строка содержит менее 128 байт, то поле **length** TLV Triplet требует только одного байта для указания длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="7a32e-108">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="7a32e-109">Если длина строки превышает 127 байт, то разряд 7 в поле **length** устанавливается в 1, а биты с 6 по 0 указывают количество дополнительных байтов, используемых для определения длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="7a32e-109">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="7a32e-110">Дополнительные сведения см. в разделе [кодированная Длина и байты значений](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="7a32e-110">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a32e-111">См. также</span><span class="sxs-lookup"><span data-stu-id="7a32e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a32e-112">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="7a32e-112">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="7a32e-113">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="7a32e-113">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



