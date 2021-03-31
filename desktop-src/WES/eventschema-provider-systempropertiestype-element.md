---
title: Элемент Provider (Системпропертиестипе)
description: Определяет поставщика, который зарегистрировал событие.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- Журнал событий элемента поставщика
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071277"
---
# <a name="provider-systempropertiestype-element"></a>Элемент Provider (Системпропертиестипе)

Определяет поставщика, который зарегистрировал событие.

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Элемент **provider** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Атрибуты



| Имя            | Тип                                                | Описание                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| евентсаурценаме | строка                                              | Имя источника события, опубликовавшего событие (если источником события является устаревший API [протоколирования событий](/windows/desktop/EventLog/event-logging) ).<br/> |
| Guid            | [**гуидтипе**](eventschema-guidtype-simpletype.md) | Глобальный уникальный идентификатор, который однозначно идентифицирует поставщик.<br/>                                                                   |
| Имя            | anyURI                                              | Имя поставщика событий, который зарегистрировал событие.<br/>                                                                                   |



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

 

