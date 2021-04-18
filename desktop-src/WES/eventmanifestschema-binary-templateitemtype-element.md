---
title: Binary (Темплатеитемтипе), элемент
description: Содержит двоичные данные, предоставляемые API журнала событий.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- Журнал событий двоичного элемента
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691908"
---
# <a name="binary-templateitemtype-element"></a>Binary (Темплатеитемтипе), элемент

Содержит двоичные данные, предоставляемые API [журнала событий](/windows/desktop/EventLog/event-logging) .

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Элемент **binary** определяется сложным типом [**темплатеитемтипе**](eventmanifestschema-templateitemtype-complextype.md) .

## <a name="attributes"></a>Атрибуты



| Имя | Тип   | Описание                                          |
|------|--------|------------------------------------------------------|
| name | строка | Имя, связанное с двоичными данными.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**шаблон (Темплателисттипе)**](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

