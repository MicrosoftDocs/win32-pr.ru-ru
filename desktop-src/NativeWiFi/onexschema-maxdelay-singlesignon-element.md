---
description: Указывает максимальную задержку в секундах, по истечении которой попытка подключения единого входа завершается неудачей.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: Максделай (singleSignOn), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909431"
---
# <a name="maxdelay-singlesignon-element"></a>Максделай (singleSignOn), элемент

Элемент Максделай (singleSignOn) указывает в секундах максимальную задержку перед неудачной попыткой подключения единого входа.

Этот элемент является необязательным. Если Максделай не указан в профиле, используется значение 10 секунд.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент **максделай** определяется элементом [**singleSignOn**](onexschema-singlesignon-onex-element.md) .

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

 

 
