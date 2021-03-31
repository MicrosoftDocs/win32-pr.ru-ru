---
title: Элемент Еаптипе (свойство соединения со схемой v1)
description: Сведения об элементе Еаптипе. Этот элемент захватывает конфигурацию, зависящую от метода, внутри элемента EAP. | Элемент Еаптипе (свойство соединения со схемой v1)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
keywords:
- Элемент Еаптипе EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820572"
---
# <a name="eaptype-element-v1-schema-connection-property"></a>Элемент Еаптипе (свойство соединения со схемой v1)

Элемент **еаптипе** фиксирует конфигурацию, относящуюся к методу, внутри элемента EAP.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Комментарии

Элемент **еаптипе** является абстрактным; Каждый метод должен определять и использовать производный элемент в документах экземпляра.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





