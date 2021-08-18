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
ms.openlocfilehash: 372163b39ea788b5c03bd25aedcc44aee172d58080fb94e3333a029a514962a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404594"
---
# <a name="innereapoptional-eaptype-element"></a>Иннереапоптионал (Еаптипе), элемент

Элемент **иннереапоптионал (еаптипе)** указывает, следует ли выполнять гостевой доступ.

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

Элемент **иннереапоптионал** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Remarks

Если элемент **иннереапоптионал** имеет значение true, то должен присутствовать элемент [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) , описывающий внутренний метод и его конфигурацию. Если задано значение FALSE, PEAP выполняет гостевой доступ. Элемент **иннереапоптионал** является необязательным.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



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

 

 





