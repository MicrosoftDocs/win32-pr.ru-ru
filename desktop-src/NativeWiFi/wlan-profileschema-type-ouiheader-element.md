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
ms.openlocfilehash: 12637e5a70409166e5a31aa0fc98f4df1b9f6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910647"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**ауихеадер**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Ауихеадер (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




