---
description: Указывает, заблокирован ли доступ ко всем сетям инфраструктуры.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: Деняллесс (Нетворкфилтер), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5057f94dd91e2d7090c4f147ba987324e369dda706031ecebb8a79b165214414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619869"
---
# <a name="denyalless-networkfilter-element"></a>Деняллесс (Нетворкфилтер), элемент

Элемент Деняллесс (Нетворкфилтер) указывает, заблокирован ли доступ ко всем сетям инфраструктуры. Если **деняллесс** имеет значение true, компьютеры не могут подключаться к сети инфраструктуры. в противном случае компьютеры могут подключаться к сетям инфраструктуры.

Значение по умолчанию для этого элемента — FALSE. Если **деняллесс** не указан в профиле, компьютеры по умолчанию могут подключаться к сетям инфраструктуры.

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

Элемент **деняллесс** определяется элементом [**нетворкфилтер**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**нетворкфилтер**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Нетворкфилтер (Вланполици)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




