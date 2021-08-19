---
description: Содержит 1-байтовый hexBinary, используемый для различения сетевых карт, созданных одним и тем же IHV.
ms.assetid: fd6bae3d-27a8-4bff-9340-b444312b8216
title: Элемент Type (Ауихеадер)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 234b30883df463d7c336ce7d270e574d41a5cabe9924c327a35ff1a31ee65632
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797505"
---
# <a name="type-ouiheader-element"></a>Элемент Type (Ауихеадер)

Элемент Type (Ауихеадер) содержит 1-байтный hexBinary, который используется для различения сетевых карт, созданных одним и тем же IHV.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.

``` syntax
<xs:element name="type">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент определяется элементом [**ауихеадер**](wlan-profileschema-ouiheader-ihv-element.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**ауихеадер**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Ауихеадер (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




