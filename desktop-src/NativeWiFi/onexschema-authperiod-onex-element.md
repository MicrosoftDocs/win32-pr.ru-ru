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
ms.openlocfilehash: ccaef08f65baffa0d7b9a921afd9db78a6ac6c6dd1d0bf4fd8075454fe38be21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684863"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



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

 

 




