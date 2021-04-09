---
title: Акцептсервернаме (Пеапекстенсионстипе), элемент
description: Указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе ServerName (Сервервалидатионпараметерс). | Акцептсервернаме (Пеапекстенсионстипе), элемент
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- элемент EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c877819fd559cb26cd93c5d5456631a93a49545
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081786"
---
# <a name="acceptservername-peapextensionstype-element"></a>Акцептсервернаме (Пеапекстенсионстипе), элемент

Элемент **акцептсервернаме (пеапекстенсионстипе)** указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе [**ServerName (сервервалидатионпараметерс)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

Элемент определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .

## <a name="remarks"></a>Комментарии

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

[Схема mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[**акцептсервернаме**](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





