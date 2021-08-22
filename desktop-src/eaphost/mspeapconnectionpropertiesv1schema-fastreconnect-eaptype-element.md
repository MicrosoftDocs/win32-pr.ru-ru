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
ms.openlocfilehash: 1bda956d698ebefef956e85557c6d940baa02f6bcc9ef7cca0081fd668107e18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119238724"
---
# <a name="fastreconnect-eaptype-element"></a>FastReconnect (Еаптипе), элемент

Элемент **FastReconnect (еаптипе)** указывает, нужно ли выполнять быстрое повторное подключение.

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

Элемент **FastReconnect** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Remarks

Если элемент **FastReconnect** имеет значение true, то PEAP пытается выполнить быстрое повторное подключение. Если значение равно FALSE, PEAP выполняет полную проверку подлинности. Элемент **FastReconnect** является необязательным.

## <a name="requirements"></a>Requirements (Требования)



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

 

 





