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
ms.openlocfilehash: e5327bc267272942df30044678a96244d957122c9fbf7878a805bfd48433e20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904532"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Система (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

