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
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694045"
---
# <a name="taskeventdefinitiontype-complex-type"></a>Сложный тип Таскевентдефинитионтипе

\[Начиная с компилятора сообщений, который поставляется с версией Windows SDK Windows 7, сложный тип Таскевентдефинитионтипе больше не доступен. Вместо этого используйте коды операций для конкретных задач, чтобы предоставить те же функциональные возможности.\]

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





