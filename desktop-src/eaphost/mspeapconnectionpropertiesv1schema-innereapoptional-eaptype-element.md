---
title: Иннереапоптионал (Еаптипе), элемент
description: Сведения об элементе Иннереапоптионал (Еаптипе). Этот элемент указывает, следует ли выполнять гостевой доступ.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Элемент Иннереапоптионал EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be63845f389936656172b4cbb4e42de659bbf0e1
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134567"
---
# <a name="innereapoptional-eaptype-element"></a>Иннереапоптионал (Еаптипе), элемент

Элемент **иннереапоптионал (еаптипе)** указывает, следует ли выполнять гостевой доступ.

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

Элемент **иннереапоптионал** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Комментарии

Если элемент **иннереапоптионал** имеет значение true, то должен присутствовать элемент [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) , описывающий внутренний метод и его конфигурацию. Если задано значение FALSE, PEAP выполняет гостевой доступ. Элемент **иннереапоптионал** является необязательным.

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

 

 





