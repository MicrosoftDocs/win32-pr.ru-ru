---
title: Сложный тип Тасклисттипе
description: Определяет список задач, которые используются для определения компонентов приложения.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- Журнал событий сложных типов Тасклисттипе
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d59457aaeeefeec4b490b4c399a2faafb4f62c22e67a600f741ccc16b3abcaad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750910"
---
# <a name="tasklisttype-complex-type"></a>Сложный тип Тасклисттипе

Определяет список задач, которые используются для определения компонентов приложения.

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                       | Тип                                                         | Описание                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**задачи**](eventmanifestschema-task-tasklisttype-element.md) | [**TaskType**](eventmanifestschema-tasktype-complextype.md) | Определяет компонент или подкомпонент приложения.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





