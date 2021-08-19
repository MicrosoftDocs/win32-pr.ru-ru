---
title: Элемент Correlation (Системпропертиестипе)
description: Идентификаторы действий, которые потребители могут использовать для группирования связанных событий.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Журнал событий элемента корреляции
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc301c43bbc8ba834949ae2a5056fb4359b5c8db3125da3d1729b18ac7aa1b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120362"
---
# <a name="correlation-systempropertiestype-element"></a>Элемент Correlation (Системпропертиестипе)

Идентификаторы действий, которые потребители могут использовать для группирования связанных событий.

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Элемент **Correlation** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Атрибуты



| Имя              | Тип                                                | Описание                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор действия        | [**гуидтипе**](eventschema-guidtype-simpletype.md) | Глобальный уникальный идентификатор, определяющий текущее действие. События, опубликованные с помощью этого идентификатора, являются частью одного действия.<br/>                              |
| RelatedActivityID | [**гуидтипе**](eventschema-guidtype-simpletype.md) | Глобальный уникальный идентификатор, определяющий действие, в которое был передан элемент управления. Затем связанные события будут иметь этот идентификатор в качестве идентификатора ActivityID.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Система (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





