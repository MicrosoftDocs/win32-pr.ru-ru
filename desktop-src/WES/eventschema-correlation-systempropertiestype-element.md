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
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989104"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Система (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





