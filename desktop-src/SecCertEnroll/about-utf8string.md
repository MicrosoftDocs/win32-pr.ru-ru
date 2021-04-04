---
description: Тип данных ASN. 1 Образец UTF8String кодируется в TLV-Triplet, который начинается с тега Byte 0x0C.
ms.assetid: e30737d3-8294-48d8-9e42-f21918acc73c
title: Образец UTF8String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26048a46689d27b68e8cacfa4af13b37cde4d613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909639"
---
# <a name="utf8string"></a><span data-ttu-id="e8baf-103">Образец UTF8String</span><span class="sxs-lookup"><span data-stu-id="e8baf-103">UTF8String</span></span>

<span data-ttu-id="e8baf-104">Тип данных ASN. 1 **Образец UTF8String** кодируется в TLV-Triplet, который начинается с **тега** Byte 0x0C.</span><span class="sxs-lookup"><span data-stu-id="e8baf-104">The ASN.1 **UTF8String** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x0C.</span></span> <span data-ttu-id="e8baf-105">В следующем примере из раздела [ASN. 1, закодированного](cmc-encoded-asn-1.md) с помощью CMC, показано, как атрибут **ClientID** кодируется как целое число и три типа **Образец UTF8String** .</span><span class="sxs-lookup"><span data-stu-id="e8baf-105">The following example, from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows how the **ClientId** attribute is encoded as an integer and three **UTF8String** types.</span></span> <span data-ttu-id="e8baf-106">Идентификатор объекта для атрибута — 1.3.6.1.4.1.311.21.20.</span><span class="sxs-lookup"><span data-stu-id="e8baf-106">The object identifier for the attribute is 1.3.6.1.4.1.311.21.20.</span></span> <span data-ttu-id="e8baf-107">Сведения, которые можно указать с помощью интерфейса [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) , включают идентификационный номер клиента, имя компьютера службы доменных имен (DNS), имя пользователя диспетчера учетных записей безопасности (SAM) и имя приложения, создавшего запрос на сертификат.</span><span class="sxs-lookup"><span data-stu-id="e8baf-107">The information, which can be specified by using the [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) interface, includes a client ID number, the Domain Name System (DNS) computer name, the Security Accounts Manager (SAM) user name, and the name of the application that created the certificate request.</span></span>

``` syntax
06 09                                ; OBJECT_ID (9 Bytes)
|  2b 06 01 04 01 82 37 15  14       ;   1.3.6.1.4.1.311.21.20 
31 4a                                ; SET (4a Bytes)
   30 48                             ; SEQUENCE (48 Bytes)
      02 01                          ; INTEGER (1 Bytes)
      |  09
      0c 23                          ; UTF8_STRING (23 Bytes)
      |  76 69 63 68 33 64 2e 6a     ;   vich3d.j
      |  64 6f 6d 63 73 63 2e 6e     ;   domcsc.n
      |  74 74 65 73 74 2e 6d 69     ;   ttest.mi
      |  63 72 6f 73 6f 66 74 2e     ;   crosoft.
      |  63 6f 6d                    ;   com
      0c 15                          ; UTF8_STRING (15 Bytes)
      |  4a 44 4f 4d 43 53 43 5c     ;   JDOMCSC\
      |  61 64 6d 69 6e 69 73 74     ;   administ
      |  72 61 74 6f 72              ;   rator
      0c 07                          ; UTF8_STRING (7 Bytes)
         63 65 72 74 72 65 71        ;   certreq
```

<span data-ttu-id="e8baf-108">Если строка содержит менее 128 байт, то поле **length** TLV Triplet требует только одного байта для указания длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="e8baf-108">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="e8baf-109">Если длина строки превышает 127 байт, то разряд 7 в поле **length** устанавливается в 1, а биты с 6 по 0 указывают количество дополнительных байтов, используемых для определения длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="e8baf-109">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="e8baf-110">Дополнительные сведения см. в разделе [кодированная Длина и байты значений](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="e8baf-110">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8baf-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e8baf-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8baf-112">Система типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="e8baf-112">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="e8baf-113">Кодировка DER для типов ASN. 1</span><span class="sxs-lookup"><span data-stu-id="e8baf-113">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



