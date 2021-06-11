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
ms.openlocfilehash: 64e82defae9c5ae9f7cf60056cfdac8b58373602
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989479"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

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

 

 





