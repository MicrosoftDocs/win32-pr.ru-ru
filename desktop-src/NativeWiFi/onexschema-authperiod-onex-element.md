---
description: Указывает максимальный интервал времени (в секундах), в течение которого клиент ожидает ответа от средства проверки подлинности.
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: Элемент Ауспериод (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 098391a672eedd2657dbd7ad5913fef13fde98cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080758"
---
# <a name="authperiod-onex-element"></a>Элемент Ауспериод (OneX)

Элемент Ауспериод (OneX) задает максимальный интервал времени в секундах, в течение которого клиент ожидает ответа от средства проверки подлинности. Если ответ не получен в течение указанного периода, клиент предполагает, что в сети отсутствует средство проверки подлинности.

Этот элемент является необязательным. Если Ауспериод не указан в профиле, используется значение 18 секунд.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.

``` syntax
<xs:element name="authPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент **ауспериод** определяется элементом [**OneX**](onexschema-onex-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**Таймаут**](onexschema-onex-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Таймаут**](onexschema-onex-element.md)
</dt> </dl>

 

 




