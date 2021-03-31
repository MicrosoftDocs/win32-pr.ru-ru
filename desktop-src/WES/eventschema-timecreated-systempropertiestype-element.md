---
title: TimeCreated (Системпропертиестипе), элемент
description: Метка времени, определяющая время записи события в журнал.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- Журнал событий элемента TimeCreated
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 998bb03601f0ecbe87c571daa94b1f33e307d6af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988841"
---
# <a name="timecreated-systempropertiestype-element"></a>TimeCreated (Системпропертиестипе), элемент

Метка времени, определяющая время записи события в журнал.

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

Элемент **TimeCreated** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Атрибуты



| Имя       | Тип     | Описание                                              |
|------------|----------|----------------------------------------------------------|
| SystemTime | dateTime | Системное время, когда событие было зарегистрировано.<br/> |



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

 

 





