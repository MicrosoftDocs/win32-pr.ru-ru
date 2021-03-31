---
title: Сложный тип Шовмессажетипе
description: Определяет элементы, представляющие действие, которое отображает окно сообщения.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- планировщик задач сложного типа Шовмессажетипе
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988947"
---
# <a name="showmessagetype-complex-type"></a>Сложный тип Шовмессажетипе

Определяет элементы, представляющие действие, которое отображает окно сообщения.

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                            | Тип           | Описание                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Текст**](taskschedulerschema-body-showmessagetype-element.md)   | нонемптистринг | Задает текст, отображаемый в тексте окна сообщения. <br/> |
| [**Заголовок**](taskschedulerschema-title-showmessagetype-element.md) | нонемптистринг | Задает заголовок окна сообщения. <br/>                       |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





