---
title: Элемент Еаптипе (базовые свойства пользователя)
description: Сведения об элементе Еаптипе. Этот элемент захватывает конфигурацию, зависящую от метода, внутри элемента EAP. | Элемент Еаптипе (базовые свойства пользователя)
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
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
ms.openlocfilehash: 5fffa74c69b5ecbf2823cfa79ae376fed524e8ca
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713399"
---
# <a name="eaptype-element-base-user-properties"></a>Элемент Еаптипе (базовые свойства пользователя)

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
|-------------------------------------|------------------------------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





