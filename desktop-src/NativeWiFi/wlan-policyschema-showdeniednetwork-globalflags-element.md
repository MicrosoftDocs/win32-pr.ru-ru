---
description: Указывает, отображаются ли запрещенные сети в мастере подключения к сети.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: Шовдениеднетворк (Глобалфлагс), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543759"
---
# <a name="showdeniednetwork-globalflags-element"></a>Шовдениеднетворк (Глобалфлагс), элемент

Элемент **шовдениеднетворк** (глобалфлагс) указывает, отображаются ли запрещенные сети в мастере **подключения к сети** . Сети могут быть отклонены групповой политикой или параметрами пользователя. Если **шовдениеднетворк** имеет значение true, в мастере **подключения к сети** отображаются запрещенные сети. в противном случае запрещенные сети не будут отображаться в мастере.

Этот элемент является обязательным. При создании профиля службой автонастройки этот элемент будет принимать значение по умолчанию FALSE.

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

Элемент **шовдениеднетворк** определяется элементом [**глобалфлагс**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**глобалфлагс**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Глобалфлагс (Вланполици)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




