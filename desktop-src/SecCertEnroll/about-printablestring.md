---
description: Тип данных ASN. 1 Принтаблестринг кодируется в TLV-Triplet, который начинается с тега Byte 0x13.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: принтаблестринг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e2714013c037e834a7c083c7ab89fcdafd59e1306226af25fcb4b6edc8b0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903756"
---
# <a name="printablestring"></a>принтаблестринг

Тип данных ASN. 1 **принтаблестринг** кодируется в TLV-Triplet, который начинается с **тега** Byte 0x13. В следующем примере из статьи [PKCS \# 10 Encoded ASN. 1](pkcs--10-encoded-asn-1.md) показано, как общее имя пользователя тесткн кодируется как тип **принтаблестринг** . Идентификатор объекта для общего имени — 2.5.4.3.

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

Если строка содержит менее 128 байт, то поле **length** TLV Triplet требует только одного байта для указания длины содержимого. Если длина строки превышает 127 байт, то разряд 7 в поле **length** устанавливается в 1, а биты с 6 по 0 указывают количество дополнительных байтов, используемых для определения длины содержимого. Дополнительные сведения см. в разделе [кодированная Длина и байты значений](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Система типов ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Кодировка DER для типов ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



