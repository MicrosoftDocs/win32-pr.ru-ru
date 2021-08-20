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
ms.openlocfilehash: 8decb1746391c1337440eb475a8a8face3f8b7466b73015db48e3991841a3c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086779"
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

## <a name="remarks"></a>Remarks

Метод EAP выполняет проверку схемы содержимого элемента **басиапмесодконфиг** .

## <a name="requirements"></a>Requirements (Требования)



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема басиапмесодконфиг](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





