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
ms.openlocfilehash: 9f34a45a0fc527c4c27e24ad3137dfe49438f9255baf1893e1090137bfb40a3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619539"
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

 

 




