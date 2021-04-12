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
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262998"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



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

 

 




