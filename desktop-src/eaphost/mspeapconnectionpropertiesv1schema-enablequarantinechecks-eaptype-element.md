---
title: Енаблекуарантинечеккс (Еаптипе), элемент
description: Сведения об элементе Енаблекуарантинечеккс (Еаптипе). Этот элемент указывает, следует ли выполнять проверки защиты доступа к сети (NAP).
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- Элемент Енаблекуарантинечеккс EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987902"
---
# <a name="enablequarantinechecks-eaptype-element"></a>Енаблекуарантинечеккс (Еаптипе), элемент

Элемент **енаблекуарантинечеккс (еаптипе)** указывает, следует ли выполнять проверки защиты доступа к сети (NAP).

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

Элемент **енаблекуарантинечеккс** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Комментарии

Если элемент **енаблекуарантинечеккс** имеет значение true, PEAP ВЫПОЛНЯЕТ проверки NAP; Если значение равно FALSE, PEAP не будет выполнять проверки защиты доступа к сети. Элемент **енаблекуарантинечеккс** является необязательным.

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

 

 





