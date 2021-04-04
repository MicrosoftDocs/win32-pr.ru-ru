---
description: Определяет список, содержащий до пяти атрибутов счетчика.
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: Сложный тип Каунтераттрибутес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfcb94b131e1343565d5763ae2ea4d95e53f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998516"
---
# <a name="counterattributes-complex-type"></a>Сложный тип Каунтераттрибутес

Определяет список, содержащий до пяти атрибутов счетчика.

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент              | Тип                                                                               | Описание                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| **каунтераттрибуте** | [**мужчина: Каунтераттрибуте**](performance-counters-counterattribute-complex-type.md) | Атрибут счетчика, указывающий способ отображения данных счетчиков в приложении-потребителе.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




