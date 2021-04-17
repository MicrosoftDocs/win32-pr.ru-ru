---
description: Указывает, заблокирован ли доступ ко всем компьютерным сетям.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: Деняллибсс (Нетворкфилтер), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673247"
---
# <a name="denyallibss-networkfilter-element"></a>Деняллибсс (Нетворкфилтер), элемент

Элемент Деняллибсс (Нетворкфилтер) указывает, заблокирован ли доступ ко всем компьютерам ad-hoc. Если **деняллибсс** имеет значение true, компьютеры не могут подключаться к сети ad-hoc; в противном случае компьютеры могут подключаться к компьютерным сетям.

Значение по умолчанию для этого элемента — FALSE. Если **деняллибсс** не указан в профиле, компьютеры по умолчанию могут подключаться к сетям с прямым подключением.

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

Элемент **деняллибсс** определяется элементом [**нетворкфилтер**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

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

 

 




