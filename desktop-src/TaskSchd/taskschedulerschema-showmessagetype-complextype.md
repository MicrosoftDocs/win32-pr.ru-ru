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
ms.openlocfilehash: aeb2c0e1b3ac3e29502e7d998305674aaa283371be6a22324dde6d84c4330326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611246"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





