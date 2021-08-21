---
title: Сложный тип Таскевентдефинитионтипе
description: Определяет событие, специфическое для задачи, которое поставщик может заносить в журнал. | Сложный тип Таскевентдефинитионтипе
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- Журнал событий сложных типов Таскевентдефинитионтипе
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44a4fc7ca8784b3472fea3b0d4f4e657ce615fae05a8cc7372aa3cca0fedb431
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055842"
---
# <a name="taskeventdefinitiontype-complex-type"></a>Сложный тип Таскевентдефинитионтипе

\[начиная с компилятора сообщений, который поставляется с версией Windows 7 Windows SDK, сложный тип таскевентдефинитионтипе больше не доступен. Вместо этого используйте коды операций для конкретных задач, чтобы предоставить те же функциональные возможности.\]

Определяет событие, специфическое для задачи, которое поставщик может заносить в журнал.

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                      | Тип                                                                               | Описание                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| **event**                                                                    | [**евентдефинитионтипе**](eventmanifestschema-eventdefinitiontype-complextype.md) | Событие, относящееся к задаче, опубликованное с помощью задачи.<br/> |
| [**транслируют**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | Код операции, относящийся к задаче, для события. <br/>   |



## <a name="attributes"></a>Атрибуты



| Имя | Тип      | Описание                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Имя кода операции, относящегося к задаче.<br/> |
| name | anyURI    | Имя данной задачи.<br/>                 |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





