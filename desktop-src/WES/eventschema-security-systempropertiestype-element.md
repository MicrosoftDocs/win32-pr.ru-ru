---
title: Элемент Security (Системпропертиестипе)
description: Указывает пользователя, который записал в журнал событие.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- Журнал событий элемента безопасности
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b793193d7afdfde5fd515252a024432ed45ff8b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137310"
---
# <a name="security-systempropertiestype-element"></a>Элемент Security (Системпропертиестипе)

Указывает пользователя, который записал в журнал событие.

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Элемент **Security** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Атрибуты



| Имя   | Тип   | Описание                                                          |
|--------|--------|----------------------------------------------------------------------|
| UserID | строка | Идентификатор безопасности (SID) пользователя в строковой форме.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Система (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





