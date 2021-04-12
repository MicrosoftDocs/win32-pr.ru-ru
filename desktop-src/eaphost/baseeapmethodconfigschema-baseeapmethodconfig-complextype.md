---
title: Сложный тип Басиапмесодконфиг
description: Сведения о сложном типе Басиапмесодконфиг. Этот тип является элементом-заполнителем для конфигурации метода.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- Басиапмесодконфиг сложный тип EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413765"
---
# <a name="baseeapmethodconfig-complex-type"></a>Сложный тип Басиапмесодконфиг

Сложный тип **басиапмесодконфиг** — это элемент-заполнитель для конфигурации метода.

``` syntax
<xs:complexType name="BaseEapMethodConfig">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Комментарии

Метод EAP выполняет проверку схемы содержимого элемента **басиапмесодконфиг** .

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема басиапмесодконфиг](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





