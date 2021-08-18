---
title: Дифферентусернаме (Еаптипе), элемент
description: Сведения об элементе Дифферентусернаме (Еаптипе). Этот элемент определяет, какое имя пользователя использует EAP-TLS.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Элемент Дифферентусернаме EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2980a55e76d238578822cfc8db54a9b6c324e21d4a8f0481ab9bc91e050fb008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984094"
---
# <a name="differentusername-eaptype-element"></a>Дифферентусернаме (Еаптипе), элемент

Элемент **дифферентусернаме (еаптипе)** определяет, какое имя пользователя использует EAP-TLS.

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

Элемент **дифферентусернаме** определяется элементом [**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Remarks

Если элемент **дифферентусернаме** имеет значение true, то EAP-TLS должен использовать имя пользователя, отличное от имени, которое отображается в сертификате. Если элемент **дифферентусернаме** имеет значение false, то EAP-TLS использует имя пользователя, которое отображается в сертификате.

Элемент **дифферентусернаме** является необязательным.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





