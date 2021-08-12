---
title: Сложный тип Дефинитионтипе
description: Определяет список событий, которые поставщик может заносить в журнал.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- Журнал событий сложных типов Дефинитионтипе
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f62ab040f57fdeb4e4208554c642e9b0bc2fb1135512d1c512f0b0ef90b69e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589639"
---
# <a name="definitiontype-complex-type"></a>Сложный тип Дефинитионтипе

Определяет список событий, которые поставщик может заносить в журнал.

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                           | Тип                                                                                       | Описание                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**журнале**](eventmanifestschema-event-definitiontype-element.md) | [**евентдефинитионтипе**](eventmanifestschema-eventdefinitiontype-complextype.md)         | Определяет событие, которое может регистрироваться поставщиком.<br/>                                                                                                                                                                                                                                 |
| [**задачи**](eventmanifestschema-task-definitiontype-element.md)   | [**таскевентдефинитионтипе**](eventmanifestschema-taskeventdefinitiontype-complextype.md) | Не поддерживается.<br/> **Windows Server 2008 и Windows Vista:** Определяет событие, специфическое для задачи, которое поставщик может заносить в журнал. (начиная с компилятора сообщений, который поставляется с версией Windows 7 Windows SDK, события, относящиеся к задачам, больше не поддерживаются.)<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





