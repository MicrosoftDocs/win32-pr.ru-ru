---
title: Рекуирекриптобиндинг (Еаптипе), элемент
description: Указывает, следует ли выполнять проверку подлинности на серверах, поддерживающих криптобиндинг.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- Элемент Рекуирекриптобиндинг EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63ee456f87205346a935ad047cb8db9828febba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415960"
---
# <a name="requirecryptobinding-eaptype-element"></a>Рекуирекриптобиндинг (Еаптипе), элемент

Элемент **рекуирекриптобиндинг (еаптипе)** указывает, следует ли выполнять проверку подлинности на серверах, поддерживающих криптобиндинг.

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

Элемент **рекуирекриптобиндинг** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Комментарии

Если элемент **рекуирекриптобиндинг** имеет значение true, PEAP будет проходить проверку подлинности на серверах, не поддерживающих криптобиндинг. Если значение равно FALSE, PEAP будет проходить проверку подлинности только на серверах, поддерживающих криптобиндинг. Элемент **рекуирекриптобиндинг** является необязательным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



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

 

 





