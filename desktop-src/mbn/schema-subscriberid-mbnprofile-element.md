---
description: Определяет уникальный идентификатор профиля.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: Субскриберид (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: 42290b0a80e85b2fdd1c794aced78571e939010b0e260bf1bdeba15f221cc103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065888"
---
# <a name="subscriberid-mbnprofile-element"></a>Субскриберид (Мбнпрофиле), элемент

Элемент **субскриберид (мбнпрофиле)** определяет уникальный идентификатор профиля.

Для сети GSM оно должно содержать IMSI (Международный идентификатор мобильного подписчика) SIM-карты и устройства CDMA, которые должны содержать минимальное значение (мобильный идентификационный номер) устройства.

Элемент — это числовая строка с максимальной длиной 15 цифр.

Элемент является обязательным.

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

Элемент **субскриберид** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




