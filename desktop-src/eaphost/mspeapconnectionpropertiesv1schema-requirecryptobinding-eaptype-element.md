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
ms.openlocfilehash: 1c4f4169e6ac0af123085795374b06de854b261b5f22004bd726ad47488bc11d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067224"
---
# <a name="requirecryptobinding-eaptype-element"></a>Рекуирекриптобиндинг (Еаптипе), элемент

Элемент **рекуирекриптобиндинг (еаптипе)** указывает, следует ли выполнять проверку подлинности на серверах, поддерживающих криптобиндинг.

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

Элемент **рекуирекриптобиндинг** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Remarks

Если элемент **рекуирекриптобиндинг** имеет значение true, PEAP будет проходить проверку подлинности на серверах, не поддерживающих криптобиндинг. Если значение равно FALSE, PEAP будет проходить проверку подлинности только на серверах, поддерживающих криптобиндинг. Элемент **рекуирекриптобиндинг** является необязательным.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

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

 

 





