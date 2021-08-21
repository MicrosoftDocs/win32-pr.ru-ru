---
title: Акцептсервернаме (Пеапекстенсионстипе), элемент
description: Элемент Акцептсервернаме (Пеапекстенсионстипе) указывает, проверяется ли имя сервера на соответствие строке имени, указанной в ServerName в схеме mspeapconnectionpropertiesv2.
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Элемент Акцептсервернаме EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b608629c9eb9d3e3fb592ead73ddc0ba9545e6b92a642adf4ce76bb0524b57ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086043"
---
# <a name="acceptservername-peapextensionstype-element"></a>Акцептсервернаме (Пеапекстенсионстипе), элемент

Элемент **акцептсервернаме (пеапекстенсионстипе)** указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе [**ServerName (сервервалидатионпараметерс)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

Элемент **акцептсервернаме** определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .

## <a name="remarks"></a>Remarks

Элемент **акцептсервернаме** является необязательным.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**пеапекстенсионс**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Элементы схемы mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





