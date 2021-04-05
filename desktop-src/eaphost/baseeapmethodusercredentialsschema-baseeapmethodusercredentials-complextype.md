---
title: Сложный тип Басиапмесодусеркредентиалс
description: Сведения о сложном типе Басиапмесодусеркредентиалс. Этот тип является элементом-заполнителем для учетных данных метода.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- Басиапмесодусеркредентиалс сложный тип EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793783"
---
# <a name="baseeapmethodusercredentials-complex-type"></a>Сложный тип Басиапмесодусеркредентиалс

Сложный тип **басиапмесодусеркредентиалс** — это элемент-заполнитель для учетных данных метода.

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
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

Метод EAP выполняет проверку схемы содержимого **басиапмесодусеркредентиалс**.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема басиапмесодусеркредентиалс](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





