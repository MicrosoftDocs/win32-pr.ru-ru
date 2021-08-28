---
title: Сложный тип Куерилисттипе
description: Определяет список запросов, которые могут содержать набор селекторов и подавления, которые используются для включения или исключения событий из результирующего набора.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- Журнал событий сложных типов Куерилисттипе
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1692427538dcd500cd4190839ffcc148c7358e0aee7f5a27b4906192a0810b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904164"
---
# <a name="querylisttype-complex-type"></a>Сложный тип Куерилисттипе

Определяет список запросов, которые могут содержать набор селекторов и подавления, которые используются для включения или исключения событий из результирующего набора.

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                  | Тип                                                   | Описание                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**Запрос**](queryschema-query-querylisttype-element.md) | [**QueryType**](queryschema-querytype-complextype.md) | Определяет набор селекторов и подавления, которые используются для включения или исключения событий из результирующего набора.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





