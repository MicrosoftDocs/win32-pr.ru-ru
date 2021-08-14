---
title: Сложный тип Хеадерфиелдтипе
description: Определяет элементы, используемые для создания поля заголовка в сообщении электронной почты.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- планировщик задач сложного типа Хеадерфиелдтипе
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78c4fb3a8ca85cea5b765fc1fc4521f968efd76e9169613dc4a1565a43ee1b36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131833"
---
# <a name="headerfieldtype-complex-type"></a>Сложный тип Хеадерфиелдтипе

Определяет элементы, используемые для создания поля заголовка в сообщении электронной почты.

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                            | Тип                                                                    | Описание                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Имя**](taskschedulerschema-name-headerfieldtype-element.md)   | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md) | Задает имя поля заголовка в сообщении электронной почты.<br/> |
| [**Значение**](taskschedulerschema-value-headerfieldtype-element.md) | **строка**                                                              | Задает значение поля заголовка в сообщении электронной почты.<br/>  |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





