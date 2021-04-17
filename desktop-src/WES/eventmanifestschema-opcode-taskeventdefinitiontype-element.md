---
title: opcode, элемент (Таскевентдефинитионтипе)
description: Содержит код операции для события, относящийся к конкретной задаче. Предполагается, что все определения кодов операций относятся к задачам, содержащим определения событий.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- Журнал событий элемента кода операции
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691934"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>opcode, элемент (Таскевентдефинитионтипе)

\[Начиная с компилятора сообщений, который поставляется с версией Windows SDK для Windows 7, этот элемент больше не доступен.\]

Содержит код операции для события, относящийся к конкретной задаче. Предполагается, что все определения кодов операций относятся к задачам, содержащим определения событий.

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

Элемент **кода операции** определяется сложным типом [**таскевентдефинитионтипе**](eventmanifestschema-taskeventdefinitiontype-complextype.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                   | Тип                                                                               | Описание                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [**журнале**](eventmanifestschema-event-opcode-element.md) | [**евентдефинитионтипе**](eventmanifestschema-eventdefinitiontype-complextype.md) | Событие, публикуемое с задачей.<br/> |



## <a name="attributes"></a>Атрибуты



| Имя | Тип      | Описание                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Имя кода операции, относящегося к задаче.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**задача (Дефинитионтипе)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





