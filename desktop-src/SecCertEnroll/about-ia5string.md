---
description: Тип данных ASN. 1 IA5tring кодируется в TLV-Triplet, который начинается с тега Byte 0x16.
ms.assetid: c1268524-4304-4c21-8f7d-f0a2826cd74e
title: IA5String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5d602f50a7a3c22cd4a57d6531603307b9f14e02c537692c200a1b19fc361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904243"
---
# <a name="ia5string"></a>IA5String

Тип данных ASN. 1 **IA5tring** кодируется в TLV-Triplet, который начинается с **тега** Byte 0x16. В следующем примере, адаптированном из раздела [ASN. 1 в формате CMC](cmc-encoded-asn-1.md) , показано, как атрибут **OSVersion** кодируется как тип **IA5tring** . Номер версии можно указать с помощью интерфейса [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) . Идентификатор объекта для атрибута — 1.3.6.1.4.1.311.13.2.3.

``` syntax
06 0a                                   ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 03       ;   1.3.6.1.4.1.311.13.2.3 
31 0c                                   ; SET (c Bytes)
   16 0a                                ; IA5_STRING (a Bytes)
      36 2e 30 2e 35 33 36 31  2e 32    ;   6.0.5361.2
```

Если строка содержит менее 128 байт, то поле **length** TLV Triplet требует только одного байта для указания длины содержимого. Если длина строки превышает 127 байт, то разряд 7 в поле **length** устанавливается в 1, а биты с 6 по 0 указывают количество дополнительных байтов, используемых для определения длины содержимого. Дополнительные сведения см. в разделе [кодированная Длина и байты значений](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Система типов ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Кодировка DER для типов ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



