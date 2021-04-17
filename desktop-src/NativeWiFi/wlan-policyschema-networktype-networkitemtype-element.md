---
description: Указывает тип сети.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Нетворктипе (Нетворкитемтипе), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674214"
---
# <a name="networktype-networkitemtype-element"></a>Нетворктипе (Нетворкитемтипе), элемент

Элемент Нетворктипе (Нетворкитемтипе) указывает тип сети. Существует два типа сетей: сети инфраструктуры (ESS) и ad-hoc Network (ИБСС).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

Элемент **нетворктипе** определяется сложным типом [**нетворкитемтипе**](wlan-policyschema-networkitemtype-complextype.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**нетворкитемтипе**](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

**Возможные непосредственные родительские элементы в экземпляре схемы**
</dt> <dt>

[**сеть (разрешенных)**](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[**сеть (списка блокировки)**](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




