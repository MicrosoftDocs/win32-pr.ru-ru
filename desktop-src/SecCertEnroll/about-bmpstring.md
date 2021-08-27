---
description: Тип данных ASN. 1 Бмпстринг, называемый \_ строкой Юникода в API регистрации сертификатов, кодируется в TLV-Triplet, который начинается с тега, состоящее из байта с тегом 0x1E.
ms.assetid: 66e4a6d8-2401-4346-9361-e145735cbe19
title: бмпстринг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 496715d380739dd68dab4266422876ecca174b9caffd3895e9c465f446d32cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904843"
---
# <a name="bmpstring"></a>бмпстринг

Тип данных ASN. 1 **бмпстринг** , называемый **\_ строкой Юникода** в API регистрации сертификатов, кодируется в TLV-Triplet, который начинается с тега, состоящее из байта с **тегом** 0x1E. В следующем примере, адаптированном из раздела [ASN. 1 в формате CMC](cmc-encoded-asn-1.md) , показана кодировка для расширения **templatename** . Имя можно указать с помощью интерфейса [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) . Идентификатор объекта для расширения — 1.3.6.1.4.1.311.13.2.1.

``` syntax
06 0a                              ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 01  ;   1.3.6.1.4.1.311.13.2.1 
31 34                              ; SET (34 Bytes)
   30 32                           ; SEQUENCE (32 Bytes)
      1e 26                        ; UNICODE_STRING (26 Bytes)
      |  00 43 00 65 00 72 00 74   ;   .C.e.r.t
      |  00 69 00 66 00 69 00 63   ;   .i.f.i.c
      |  00 61 00 74 00 65 00 54   ;   .a.t.e.T
      |  00 65 00 6d 00 70 00 6c   ;   .e.m.p.l
      |  00 61 00 74 00 65         ;   .a.t.e
      1e 08                        ; UNICODE_STRING (8 Bytes)
         00 55 00 73 00 65 00 72   ;   .U.s.e.r
```

Если строка содержит менее 128 байт, то поле **length** TLV Triplet требует только одного байта для указания длины содержимого. Если длина строки превышает 127 байт, то разряд 7 в поле **length** устанавливается в 1, а биты с 6 по 0 указывают количество дополнительных байтов, используемых для определения длины содержимого. Дополнительные сведения см. в разделе [кодированная Длина и байты значений](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Система типов ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Кодировка DER для типов ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



