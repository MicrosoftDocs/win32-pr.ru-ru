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
ms.openlocfilehash: 82fbf7ec7db6f64f1bac9776376fa8fe89659d9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691830"
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
| [**задачи**](eventmanifestschema-task-definitiontype-element.md)   | [**таскевентдефинитионтипе**](eventmanifestschema-taskeventdefinitiontype-complextype.md) | Не поддерживается.<br/> **Windows Server 2008 и Windows Vista:** Определяет событие, специфическое для задачи, которое поставщик может заносить в журнал. (Начиная с компилятора сообщений, который поставляется с версией Windows 7 Windows SDK, события, относящиеся к задачам, больше не поддерживаются.)<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





