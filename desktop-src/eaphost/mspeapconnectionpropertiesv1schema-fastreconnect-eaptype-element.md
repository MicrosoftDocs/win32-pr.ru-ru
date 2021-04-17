---
title: FastReconnect (Еаптипе), элемент
description: Сведения об элементе FastReconnect (Еаптипе). Этот элемент указывает, следует ли выполнять быстрое повторное подключение.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Элемент FastReconnect EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2214519db68b8c95b0e0efa91d68a7cd667b5f87
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105691660"
---
# <a name="fastreconnect-eaptype-element"></a>FastReconnect (Еаптипе), элемент

Элемент **FastReconnect (еаптипе)** указывает, нужно ли выполнять быстрое повторное подключение.

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

Элемент **FastReconnect** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Комментарии

Если элемент **FastReconnect** имеет значение true, то PEAP пытается выполнить быстрое повторное подключение. Если значение равно FALSE, PEAP выполняет полную проверку подлинности. Элемент **FastReconnect** является необязательным.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





