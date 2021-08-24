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
ms.openlocfilehash: 7f3923e0a42375ac7d926d418943af81cc0264e111e6bdc4be56919780dfacf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652154"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>opcode, элемент (Таскевентдефинитионтипе)

\[начиная с компилятора сообщений, который поставляется с версией Windows 7 Windows SDK, этот элемент больше не доступен.\]

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**задача (Дефинитионтипе)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





