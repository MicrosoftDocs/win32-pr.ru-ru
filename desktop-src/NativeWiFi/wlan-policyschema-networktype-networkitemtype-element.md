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
ms.openlocfilehash: 57616d6701ab4663fa6757ddec5df4886ec02faaf5088f61b6cb466ca834ec81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684394"
---
# <a name="networktype-networkitemtype-element"></a>Нетворктипе (Нетворкитемтипе), элемент

Элемент Нетворктипе (Нетворкитемтипе) указывает тип сети. Существует два типа сетей: сети инфраструктуры (ESS) и ad-hoc Network (ИБСС).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

Элемент **нетворктипе** определяется сложным типом [**нетворкитемтипе**](wlan-policyschema-networkitemtype-complextype.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

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

 

 




