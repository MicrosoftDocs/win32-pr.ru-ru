---
description: Указывает, изменяется ли виртуальная локальная сеть (VLAN), используемая устройством, на основе учетных данных пользователя.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: Усербаседвиртуаллан (singleSignOn), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154578"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a>Усербаседвиртуаллан (singleSignOn), элемент

Элемент Усербаседвиртуаллан (singleSignOn) указывает, изменяется ли виртуальная локальная сеть (VLAN), используемая устройством, на основе учетных данных пользователя. Некоторые устройства сервера сетевого доступа (NAS) изменяют виртуальную локальную сеть после проверки подлинности пользователя. Когда Усербаседвиртуаллан имеет значение TRUE, NAS может изменить виртуальную ЛС устройства после проверки подлинности пользователя.

Этот элемент является необязательным. Если Усербаседвиртуаллан не указан в профиле, используется значение FALSE.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

Элемент **усербаседвиртуаллан** определяется элементом [**singleSignOn**](onexschema-singlesignon-onex-element.md) .

## <a name="remarks"></a>Комментарии

Этот параметр можно задать в командной строке с помощью команды **netsh wlan set профилепараметер** . Дополнительные сведения см. в разделе [команды Netsh для беспроводной локальной сети (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
